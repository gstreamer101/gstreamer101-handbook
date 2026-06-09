# GStreamer101 Handbook

GStreamer는 강력하지만 처음 배우는 사람에게는 용어도 개념도 낯섭니다.  
`pad`, `caps`, `bin`, `element`, `pipeline`, `bus` … 이런 용어들의 개념과 사용 방법이 많은 입문자가 GStreamer에 쉽게 다가가지 못하는 이유입니다.

**GStreamer101 Handbook**은 그 진입 장벽을 낮추기 위해 만들었습니다.  
"동작하는 코드"를 공유하는 데 그치지 않고, **"왜 이렇게 동작하는가"** 를 끝까지 설명합니다.

---

## 작성 원칙

- **입문자 기준:** "당연히 알겠지"를 가정하지 않습니다. 처음 나오는 용어는 반드시 풀어서 설명합니다.
- **이유까지 설명:** 코드를 한 줄씩 뜯어보며 "왜 이렇게 쓰는지"를 함께 다룹니다.
- **바로 실행:** 모든 예제는 실제로 빌드·실행되며, 기대 출력까지 적어 둡니다.
- **에러를 미리 안내:** 초심자가 흔히 만나는 에러와 해결책을 함께 정리합니다.

> 모든 결정의 기준은 **"입문자가 혼자 읽어도 이해되는가?"** 입니다.

---

## 무엇을 다루나

- **기반(Base):** [GStreamer 공식 Basic Tutorial](https://gstreamer.freedesktop.org/documentation/tutorials/basic/index.html)을 한국어 학습자 관점에서 풀어 씁니다.
- **확장(Extended):** 공식 튜토리얼에 없는 예제는 **GStreamer101 커뮤니티가 독자적으로 작성**해 기록합니다.

예제는 C(공식 튜토리얼 스타일)와 Python(PyGObject)을 기준으로 하며, GStreamer **1.x(1.0 API)** 를 따릅니다.

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

---

## 목차

예제가 추가되면 이 목차에 함께 등록합니다.

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

이 저장소는 **커뮤니티 기반 학습 자료**입니다. 누구나 예제를 추가하고 다듬을 수 있습니다.

- 작업 규칙·예제 작성 가이드: [`AGENTS.md`](./AGENTS.md)
- 예제 추가/수정 시 점검 리스트: [`CHECKLIST.md`](./CHECKLIST.md)

---

## 라이선스

이 핸드북은 [Creative Commons Attribution-ShareAlike 4.0 International License](./LICENSE.md), 즉 **CC BY-SA 4.0**으로 배포합니다.

자료를 공유하거나 수정해 사용할 수 있지만, 출처를 표시해야 하며 수정한 결과물도 같은 조건으로 공유해야 합니다.

---

## 참고 링크

- [GStreamer 공식 문서](https://gstreamer.freedesktop.org/documentation/)
- [Basic Tutorial](https://gstreamer.freedesktop.org/documentation/tutorials/basic/index.html)
- [핵심 개념(Foundations)](https://gstreamer.freedesktop.org/documentation/application-development/introduction/index.html)
