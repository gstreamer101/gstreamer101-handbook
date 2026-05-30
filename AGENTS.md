# GStreamer101 Handbook

> GStreamer를 처음 접하는 사람도 막힘 없이 따라올 수 있도록, **가장 쉽고 가장 친절한** GStreamer 입문 핸드북을 만드는 저장소입니다.

이 문서는 사람과 AI 에이전트 모두를 위한 **공통 작업 가이드(single source of truth)** 입니다.
`CLAUDE.md`는 이 파일을 include 하므로, 규칙·관례·구조에 대한 내용은 항상 이 `AGENTS.md`에 기록하세요.

---

## 1. 이 저장소는 무엇인가

GStreamer101 Handbook은 GStreamer의 **대중화**와 **진입 장벽 낮추기**를 목표로 하는 커뮤니티 기반 학습 저장소입니다.

- **기반(Base):** [GStreamer 공식 Basic Tutorial](https://gstreamer.freedesktop.org/documentation/tutorials/basic/index.html)을 한국어 학습자 관점에서 풀어 씁니다.
- **확장(Extended):** 공식 튜토리얼에 없는 예제는 **GStreamer101 커뮤니티가 독자적으로 작성**하여 기록합니다.
- **철학(Philosophy):** "왜 이렇게 동작하는가"를 끝까지 설명합니다. 동작하는 코드를 던지고 끝내지 않습니다.

> 핵심 원칙 한 줄: **"입문자가 혼자 읽어도 이해되는가?"** — 모든 결정의 기준입니다.

---

## 2. 독자(Audience)

- GStreamer를 **처음** 접하는 개발자
- 멀티미디어/스트리밍 도메인 지식이 거의 없는 사람
- C 또는 Python을 어느 정도 읽을 수 있으나 GStreamer 용어(pad, caps, bin, pipeline 등)는 모르는 사람

이 독자를 항상 머릿속에 두고 작성하세요. **"당연히 알겠지"를 가정하지 않습니다.**

---

## 3. 디렉토리 구조

```
gstreamer101-handbook/
├── AGENTS.md            # 공통 작업 가이드 (이 파일)
├── CLAUDE.md            # AGENTS.md를 include 하는 진입점
├── CHECKLIST.md         # 새 예제 추가 시 점검 리스트
├── README.md            # 저장소 소개 및 목차 (생성 예정)
├── tutorials/
│   ├── basic/           # 공식 Basic Tutorial 기반 예제 (basic-01, basic-02, ...)
│   └── community/       # GStreamer101 커뮤니티 독자 예제
└── docs/                # 개념 설명, 용어집, 트러블슈팅 등 보조 문서
```

> 디렉토리가 아직 없다면 첫 예제를 추가할 때 생성하세요. 구조를 바꿀 경우 이 섹션을 함께 갱신합니다.

### 예제 디렉토리 명명 규칙

- 공식 기반 예제: `tutorials/basic/basic-NN-짧은-제목/` (예: `basic-01-hello-world/`)
- 커뮤니티 예제: `tutorials/community/짧은-제목/` (예: `community/rtsp-server-minimal/`)
- 번호는 두 자리(`01`, `02`)로 0-패딩하여 정렬을 유지합니다.

---

## 4. 예제 작성 규칙 (가장 중요)

예제의 설명은 **최대한 상세하고 쉽게** 작성합니다. 각 예제 디렉토리는 다음을 포함합니다.

1. **`README.md`** — 예제 설명 문서. 아래 구조를 따릅니다.
2. **소스 코드** — `main.c` / `main.py` 등. 동작하는 완전한 코드.
3. **(선택) 빌드/실행 스크립트** — `Makefile`, `run.sh` 등.

### 예제 README.md 권장 구조

```markdown
# basic-NN: 제목

## 한 줄 요약
이 예제로 무엇을 배우는지 한 문장.

## 배경 지식
이 예제를 이해하는 데 필요한 GStreamer 개념을 입문자 눈높이로 설명.
(처음 등장하는 용어는 반드시 풀어서 설명한다)

## 전체 코드
전체 소스를 한 번에 보여준다.

## 코드 한 줄씩 뜯어보기
핵심 라인을 인용하며 "왜" 이렇게 쓰는지 설명한다.

## 실행 방법
빌드/실행 명령과 기대 출력. 복붙으로 바로 따라할 수 있게.

## 자주 막히는 부분 (Troubleshooting)
초심자가 흔히 만나는 에러와 해결책.

## 더 나아가기
다음에 볼 예제 / 관련 공식 문서 링크.
```

### 서술 원칙

- **용어를 처음 쓸 때 반드시 정의한다.** (pad, caps, bin, element, pipeline, bus 등)
- **비유와 그림말**을 적극 활용한다. (예: "pipeline은 공장의 컨베이어 벨트, element는 각 작업 기계")
- **결과를 보여준다.** 명령을 실행하면 어떤 출력이 나오는지 적는다.
- **에러 상황을 미리 알려준다.** "이렇게 하면 이런 에러가 납니다" → 입문자의 좌절을 줄인다.
- **공식 문서를 출처로 링크**하되, 그대로 번역하지 말고 **풀어서** 설명한다.
- 코드 주석도 친절하게. "무엇을" 보다 "왜"를 적는다.

---

## 5. 코드 스타일

- **C 예제:** GStreamer 공식 튜토리얼 스타일을 따른다 (`gst_*` API, `GMainLoop`, `GstBus` 패턴).
- **Python 예제:** `PyGObject`(`gi.repository.Gst`)를 사용한다.
- GStreamer 버전은 **1.x(GStreamer 1.0 API)** 를 기준으로 한다. 1.0 미만 API는 쓰지 않는다.
- 코드는 **실제로 빌드/실행되는 것만** 커밋한다. 의사코드는 본문 설명에만 사용한다.

---

## 6. 기여 / 작업 흐름

1. 새 예제는 위 디렉토리 규칙에 맞춰 추가한다.
2. 추가 전·후로 **`CHECKLIST.md`** 를 점검한다.
3. 가능한 한 예제를 **실제로 실행**해 출력 결과를 README에 반영한다.
4. 커밋 메시지는 무엇을 추가/수정했는지 명확히 적는다. (예: `add basic-01 hello world tutorial`)

---

## 7. 출처 표기 원칙

- 이 저장소의 문서와 예제는 **CC BY-SA 4.0**으로 배포한다. 자세한 내용은 `LICENSE.md`를 따른다.
- 공식 Basic Tutorial을 기반으로 한 예제는 README 하단에 **원본 링크**를 남긴다.
- 커뮤니티 독자 예제는 "GStreamer101 커뮤니티 독자 작성"임을 명시한다.
- 라이선스/저작권을 존중한다. 공식 예제 코드를 그대로 복제하지 않고, 학습용으로 재구성한다.

---

## 8. 참고 링크

- GStreamer 공식 문서: https://gstreamer.freedesktop.org/documentation/
- Basic Tutorial: https://gstreamer.freedesktop.org/documentation/tutorials/basic/index.html
- 핵심 개념(Foundations): https://gstreamer.freedesktop.org/documentation/application-development/introduction/index.html
