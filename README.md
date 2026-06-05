# GStreamer101 Handbook

> GStreamer를 처음 배우는 사람을 위한 한국어 입문서입니다.

GStreamer는 멀티미디어 처리에 강력하지만, 처음 배우기는 만만치 않습니다.
공식 문서를 펴자마자 `pad`, `caps`, `bin`, `element`, `pipeline`, `bus` 같은 용어가 쏟아지고, 많은 입문자가 여기서 한 번 멈춰 섭니다.

GStreamer101 Handbook은 그 첫 벽을 낮추려고 시작했습니다.
동작하는 코드만 던지고 끝내는 대신, 그 코드가 왜 그렇게 생겼는지를 한 줄씩 풀어 설명합니다.

---

## 이 핸드북의 방향

- 처음 보는 용어는 그때그때 풀어서 설명합니다. "당연히 알겠지"라고 넘기지 않습니다.
- 예제는 한 줄씩 짚어 가며, 왜 이렇게 쓰는지 함께 다룹니다.
- 모든 코드는 실제로 빌드·실행되며, 기대 출력까지 적어 둡니다.
- 입문자가 자주 만나는 에러와 해결책도 함께 정리합니다.

판단 기준은 하나입니다 — "입문자가 혼자 읽어도 이해되는가?"

---

## 무엇을 다루나

공식 [GStreamer Basic Tutorial](https://gstreamer.freedesktop.org/documentation/tutorials/basic/index.html)을 한국어 학습자의 시각으로 다시 풀어 씁니다.
공식 튜토리얼에 없는 주제는 GStreamer101 커뮤니티가 직접 예제를 만들어 보탭니다.

예제는 C(공식 튜토리얼 스타일)와 Python(PyGObject)을 함께 다루며, GStreamer 1.x(1.0 API)를 기준으로 합니다.

---

## 시작하기 전에

GStreamer 1.x 런타임과 개발 패키지가 필요합니다.

```bash
# Ubuntu / Debian
sudo apt install libgstreamer1.0-dev gstreamer1.0-tools \
     gstreamer1.0-plugins-base gstreamer1.0-plugins-good

# macOS (Homebrew)
brew install gstreamer gst-plugins-base gst-plugins-good

# 설치 확인
gst-launch-1.0 --version
```

빌드와 실행 명령, 기대 출력은 각 예제 README의 "실행 방법" 항목에 정리되어 있으니, 그대로 따라오면 됩니다.

---

## 목차

새 예제가 추가되면 아래 표에 함께 등록합니다.

### Basic Tutorial (공식 기반)

| # | 제목 | 무엇을 배우나 |
|---|------|---------------|
| _준비 중_ | | |

### Community (커뮤니티 독자 예제)

| 제목 | 무엇을 배우나 |
|------|---------------|
| _준비 중_ | |

---

## 함께 만들기

이 저장소는 커뮤니티가 함께 만드는 학습 자료입니다. 누구나 예제를 더하고 다듬을 수 있습니다.

- 작업 규칙과 예제 작성 가이드: [`AGENTS.md`](./AGENTS.md)
- 예제를 더하거나 고칠 때 점검할 항목: [`CHECKLIST.md`](./CHECKLIST.md)

새 예제를 쓸 때는 입문자가 혼자 읽어도 따라올 수 있도록, 가능한 한 자세하고 친절하게 풀어 주세요.

---

## 라이선스

이 핸드북은 [Creative Commons Attribution-ShareAlike 4.0 International License](./LICENSE.md), 즉 **CC BY-SA 4.0**으로 배포합니다.

자료를 공유하거나 수정해 사용할 수 있지만, 출처를 표시해야 하며 수정한 결과물도 같은 조건으로 공유해야 합니다.

---

## 참고 링크

- [GStreamer 공식 문서](https://gstreamer.freedesktop.org/documentation/)
- [Basic Tutorial](https://gstreamer.freedesktop.org/documentation/tutorials/basic/index.html)
- [핵심 개념(Foundations)](https://gstreamer.freedesktop.org/documentation/application-development/introduction/index.html)
