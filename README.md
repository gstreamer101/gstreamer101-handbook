# GStreamer101 Handbook

> 처음 GStreamer를 만지는 사람도 막힘없이 따라올 수 있도록, 쉽고 친절하게 풀어 쓴 입문 핸드북입니다.

GStreamer는 강력한 만큼 처음 보는 사람에게는 용어부터 낯섭니다.
공식 문서를 펴면 `pad`, `caps`, `bin`, `element`, `pipeline`, `bus` 같은 단어가 줄줄이 등장하고, 많은 입문자가 여기서 책을 덮습니다.

이 핸드북은 그 첫 페이지의 벽을 낮추기 위해 시작됐습니다.
그냥 돌아가는 코드만 던지는 대신, **"왜 이렇게 돌아가는가"** 를 끝까지 설명하는 것을 목표로 합니다.

---

## 이 핸드북의 약속

- **입문자 기준으로 씁니다.** "당연히 알겠지"는 없습니다. 처음 나오는 용어는 그때그때 풀어서 설명합니다.
- **"왜"를 설명합니다.** 코드를 한 줄씩 뜯어보며 어떻게가 아니라 왜 그렇게 쓰는지를 함께 다룹니다.
- **바로 실행됩니다.** 모든 예제는 실제로 빌드·실행되며, 기대 출력까지 적어 둡니다.
- **에러를 미리 알려줍니다.** 초심자가 자주 만나는 에러와 해결책을 함께 정리합니다.

> 모든 결정의 기준은 하나입니다 — **"입문자가 혼자 읽어도 이해되는가?"**

---

## 무엇을 다루나

- **기반(Base)** — [GStreamer 공식 Basic Tutorial](https://gstreamer.freedesktop.org/documentation/tutorials/basic/index.html)을 한국어 학습자의 시선으로 풀어 씁니다.
- **확장(Extended)** — 공식 튜토리얼에 없는 예제는 GStreamer101 커뮤니티가 직접 작성해 기록합니다.

예제는 C(공식 튜토리얼 스타일)와 Python(PyGObject) 두 언어로 제공하며, GStreamer 버전은 **1.x(1.0 API)** 를 기준으로 합니다.

---

## 시작하기 전에

GStreamer 1.x 런타임과 개발 패키지가 먼저 설치되어 있어야 합니다.

```bash
# Ubuntu / Debian
sudo apt install libgstreamer1.0-dev gstreamer1.0-tools \
     gstreamer1.0-plugins-base gstreamer1.0-plugins-good

# macOS (Homebrew)
brew install gstreamer gst-plugins-base gst-plugins-good

# 설치 확인
gst-launch-1.0 --version
```

> 빌드·실행 명령과 기대 출력은 각 예제 README의 **실행 방법** 섹션에 적혀 있습니다. 그대로 따라 하면 됩니다.

---

## 목차

> 새 예제가 추가되면 이 목차에도 함께 등록합니다.

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

이 저장소는 커뮤니티가 함께 만드는 학습 자료입니다. 누구나 예제를 추가하고 다듬을 수 있습니다.

- 작업 규칙과 예제 작성 가이드: [`AGENTS.md`](./AGENTS.md)
- 예제 추가·수정 시 점검 리스트: [`CHECKLIST.md`](./CHECKLIST.md)

새 예제를 쓸 때는 **입문자가 혼자 읽어도 이해되도록** 친절하게 풀어 주세요.

---

## 참고 링크

- [GStreamer 공식 문서](https://gstreamer.freedesktop.org/documentation/)
- [Basic Tutorial](https://gstreamer.freedesktop.org/documentation/tutorials/basic/index.html)
- [핵심 개념(Foundations)](https://gstreamer.freedesktop.org/documentation/application-development/introduction/index.html)
