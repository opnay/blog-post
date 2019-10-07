---
template: 'BlogPost'

thumb: "data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzAwIiBoZWlnaHQ9IjMwMCIgdmlld0JveD0iMCAwIDMwMCAzMDAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxyZWN0IHdpZHRoPSI3NTAiIGhlaWdodD0iMzAwIiBmaWxsPSJ3aGl0ZSIvPgo8bWFzayBpZD0ibWFzazAiIG1hc2stdHlwZT0iYWxwaGEiIG1hc2tVbml0cz0idXNlclNwYWNlT25Vc2UiIHg9IjAiIHk9IjAiIHdpZHRoPSIzMDAiIGhlaWdodD0iMzAwIj4KPHJlY3Qgd2lkdGg9IjMwMCIgaGVpZ2h0PSIzMDAiIGZpbGw9IiNDNEM0QzQiLz4KPC9tYXNrPgo8ZyBtYXNrPSJ1cmwoI21hc2swKSI+CjxyZWN0IHdpZHRoPSI3NTAiIGhlaWdodD0iMzAwIiBmaWxsPSJ1cmwoI3BhaW50MF9saW5lYXIpIi8+CjxwYXRoIGQ9Ik0xNTAgOTBIOTBWMTUwTDE1MCA5MFoiIGZpbGw9InVybCgjcGFpbnQxX2xpbmVhcikiLz4KPHBhdGggZD0iTTkwIDE1MEwxNTAgOTBIMjEwTDkwIDIxMFYxNTBaIiBmaWxsPSJ1cmwoI3BhaW50Ml9saW5lYXIpIi8+CjxwYXRoIGQ9Ik0xNTAgMTUwTDkwIDIxMEgyMTBMMTUwIDE1MFoiIGZpbGw9InVybCgjcGFpbnQzX2xpbmVhcikiLz4KPC9nPgo8ZGVmcz4KPGxpbmVhckdyYWRpZW50IGlkPSJwYWludDBfbGluZWFyIiB4MT0iMjk5IiB5MT0iLTUuMzE2NzNlLTA2IiB4Mj0iMi44Mjc0OGUtMDUiIHkyPSIzMDAiIGdyYWRpZW50VW5pdHM9InVzZXJTcGFjZU9uVXNlIj4KPHN0b3Agc3RvcC1jb2xvcj0iIzU4Q0ZGQiIvPgo8c3RvcCBvZmZzZXQ9IjEiIHN0b3AtY29sb3I9IiNGMEZGMDAiLz4KPC9saW5lYXJHcmFkaWVudD4KPGxpbmVhckdyYWRpZW50IGlkPSJwYWludDFfbGluZWFyIiB4MT0iMTYzLjIiIHkxPSI3Ni44IiB4Mj0iOTAiIHkyPSIxNTAiIGdyYWRpZW50VW5pdHM9InVzZXJTcGFjZU9uVXNlIj4KPHN0b3Agc3RvcC1jb2xvcj0iI0ZGNkZEOCIvPgo8c3RvcCBvZmZzZXQ9IjAuNTE5MzM3IiBzdG9wLWNvbG9yPSIjM0M4Q0U3Ii8+CjxzdG9wIG9mZnNldD0iMSIgc3RvcC1jb2xvcj0iIzAwRUFGRiIvPgo8L2xpbmVhckdyYWRpZW50Pgo8bGluZWFyR3JhZGllbnQgaWQ9InBhaW50Ml9saW5lYXIiIHgxPSIxNTAiIHkxPSI5MCIgeDI9IjkwIiB5Mj0iMTUwIiBncmFkaWVudFVuaXRzPSJ1c2VyU3BhY2VPblVzZSI+CjxzdG9wIHN0b3AtY29sb3I9IiNGQjg1NDUiLz4KPHN0b3Agb2Zmc2V0PSIxIiBzdG9wLWNvbG9yPSIjRkY2RkQ4Ii8+CjwvbGluZWFyR3JhZGllbnQ+CjxsaW5lYXJHcmFkaWVudCBpZD0icGFpbnQzX2xpbmVhciIgeDE9IjE2MC44IiB5MT0iMTM5LjIiIHgyPSI5MCIgeTI9IjIxMCIgZ3JhZGllbnRVbml0cz0idXNlclNwYWNlT25Vc2UiPgo8c3RvcCBzdG9wLWNvbG9yPSIjRkY2RkQ4Ii8+CjxzdG9wIG9mZnNldD0iMC4zMzYwMiIgc3RvcC1jb2xvcj0iIzNDOENFNyIvPgo8c3RvcCBvZmZzZXQ9IjEiIHN0b3AtY29sb3I9IiMwMEVBRkYiLz4KPC9saW5lYXJHcmFkaWVudD4KPC9kZWZzPgo8L3N2Zz4K"
title: "Kotlin 표준 함수 마스터하기"
category: "Kotlin"
date: "2018-10-22 22:52"
image: "/assets/thumb/kotlin.svg"
---
<p style="text-align:center;"><img src="{{ site.url }}/assets/kotlin/kotlin.svg" alt="Kotlin" style="height:150px;"></p>

※ 본 게시글은 해외 포스팅을 번역한 글입니다.<br>
원본 : [Elye's Medium](https://medium.com/@elye.project/mastering-kotlin-standard-functions-run-with-let-also-and-apply-9cd334b0ef84)

코틀린에는 어떻게 사용해야할지 확실하지 않을 정도로 유사한 표준함수가 있습니다.
이들의 차이점과 어떤걸 선택해야하는지 명확하게 구별하는 쉬운방법을 소개하겠습니다.

# 스코프 함수
저는 *run, with, T.run, T.let, T.also* 그리고 *T.apply*에 초점을 맞췄습니다. 저는 호출 함수의 내부 스코프를 제공하는 것처럼 주요기능을 볼때 **스코프 함수**라 부릅니다.

스코프 함수인 run함수를 쉬운방법으로 설명해드리겠습니다.

{% include services/gist.html src="0df9ada5d40f58bbeb27f7c9143a3c99" %}

`test`함수의 내부를 보면, `mood`를 출력전에 `I am happy`라고 재정의한 격리된 스코프가 있고, 이는 완전히 격리된 `run` 스코프입니다.

이 스코프 함수 자체로는 매우 유용해 보이진 않습니다. 하지만 스코프보다 좋은 것이있습니다. 스코프의 마지막 객체를 반환하는 것입니다.

아래의 적절한 예제로, 두개의 뷰에 두번 사용하지 않고 `show()`를 사용할 수 있습니다.

{% include services/gist.html src="7be24605114325be6e84ad092f58b15e" %}

# 스코프 함수의 3가지 속성
스코프 함수들을 좀더 흥미롭게 만들려면, 3가지 속성을 분류하세요.
저는 이런 속성들을 각각 구분하기 위해 사용할 것입니다.

## 1. 일반 vs 확장 함수
`with`와 `T.run`를 보면, 두 함수 모두 실제로 꽤 비슷합니다. 아래의 예제도 같습니다.

{% include services/gist.html src="9fee472457d333b07a7ecb51439be027" %}

그러나, 둘의 차이는 `with`는 일반 함수고, `T.run`은 확장 함수입니다.

그럼 질문, 각각의 이점은 무엇일까요?

`webview.settings`가 null이 될 수 있다고 생각해보면, 아래와 같이 보일겁니다.

{% include services/gist.html src="d8795e837ef2b8ea82dd322c09fca8fb" %}

**이경우, 확실히 `T.run` 확장 함수가 사용하기 전에 null 체크를 적용할 수 있어 더 낫습니다.**

## 2. 매개변수 `this` vs `it`
`T.run`과 `T.let`을 본다면, 두 함수 모두 매개 변수를 받는 것을 제외하고 닮았습니다.
아래의 예제는 두 함수 모두 같은 로직입니다.

{% include services/gist.html src="1454c5e68527b050917d4db8aa3cee71" %}

`T.run`함수의 기호를 확인해보면, `T.run`은 `block: T.()`으로 보이는 확장함수로 만들어진 것을 알 수 있습니다. 그런 까닭에 스코프 내의 모든 곳에서 `T`는 `this`로 부를 수 있습니다. 프로그래밍에서, `this`는 대부분에서 생략될 수 있습니다. 그러므로 위의 예제에서, `println`에서 `${this.length}`대신, `length`로 사용할 수 있습니다. 저는 이를 ***this를 매개변수***로 보낸다고 부릅니다.

그러나 `T.let`함수의 기호에서, `T.let`은 자기자신을 `block: (T)`인 함수로 보낸다는걸 알 수 있습니다. 그런 까닭에 이는 람다 매개변수로 보내는 것 같습니다. 스코프 내에서는 `it`으로 불릴 수 있습니다. 따라서 저는 ***it을 매개변수***로 보낸다 부릅니다.

위에서는, `T.run`이 `T.let`보다 함축적으로 더 유용한 것으로 보입니다만, `T.let` 함수에는 아래와 같이 눈에 띄지않는 장점들이 있습니다.

- `T.let`은 넘겨진 함수/멤버 변수인지, 외부 클래스의 함수/멤버 변수인지 명확하게 구분됩니다.
- `this`가 생략되지 않는 상황에서, 예를들어 함수의 파라미터로 넘겨졌을 때, `it`은 `this`보다 짧게 쓸 수 있고, 보다 깔끔합니다.
- `T.let`은 변수를 보다 나은 이름으로 바꿀 수 있습니다. 즉, `it`을 다른 이름으로 변환할 수 있습니다.

{% include services/gist.html src="17e24f833ee329c500e75803f785a7a7" %}

## 3. `this` vs 다른 타입 반환
이제, `T.let`과 `T.also`를 살펴보면, 함수 내부의 스코프를 본다면, 둘다 똑같습니다.

{% include services/gist.html src="f7c8c2a738f3e81e7c4a7ef971d11a2b" %}

그러나 그것들의 반환값이 파악하기 힘들게 다릅니다. `T.let`은 다른 타입의 값을 반환하지만, `T.also`는 `T` 자기 자신 즉, `this`를 반환합니다.

둘다 체이닝 함수(chaining function)에서는 유용합니다. `T.let`은 조작을 진화시켜주고, `T.also`는 같은 변수 즉, `this`를 사용하게 해줍니다.

아래의 간단한 실제 예제가 있습니다.

{% include services/gist.html src="0f664fa3907e7492d6300996d608a182" %}

위의 `T.also`는 의미 없어 보이며, 쉽게 함수의 한개의 블럭으로 합칠 수 있습니다. 잘 생각해보면, 약간의 장점이 있습니다.

1. 같은 객체에서 작업을 깔끔하게 분리할 수 있습니다. 즉, 함수의 영역을 작게 만들수 있습니다.
2. 사용전에 체인 빌드 기능을 만드는 것에서 자기자신을 교묘히 다루는 것을 매우 강력해질 수 있습니다.

체인을 합칠때 즉, 자기자신을 진화하고, 유지할때 아래와 같이 매우 강력해질 겁니다. 

{% include services/gist.html src="409992bceec59eb74a3a6a60d1f13ecc" %}

# 모든 속성 보기
3개의 속성을 보면, 함수의 행동을 거의 알 수 있습니다. `T.apply` 위에서 말한것과 다르게, 함수를 설명해 봅시다. 아래에 `T.apply`의 3가지 속성이 있습니다.

1. 확장 함수 입니다.
2. `this`를 매개변수로 보냅니다.
3. `this`(즉, 자기자신)을 반환합니다.

여기서 부터 사용해보면, 한가지로 아래와같이 상상할 수 있습니다.

{% include services/gist.html src="e9c7ca9f452e1a4cf1c1044c7fc55950" %}

또는 체인되지 않은 객체를 체인할 수 있게 만들 수 있습니다.

{% include services/gist.html src="d7ad797cccfd0b969cbfd613ab877f2a" %}

# 함수 선택
명백히 이제 3개의 속성으로, 함수들을 카테고리로 나눌 수 있습니다. 그리고 이것으로, 우리가 필요할때 어떤 함수를 사용해야 하는지 결정을 도와줄 수 있는 아래와 같은 결정 트리 형식을 만들 수 있습니다.

<p style="text-align:center;"><img src="{{ site.url }}/assets/kotlin/function_choose_flowchart.png" alt="Kotlin" style="width:100%;"></p>

---

오역, 의역 등 문제점이 있을 수 있습니다. 이러한 경우 댓글로 알려주시기 바랍니다.

처음 번역해 올려보는거라 이미지가 번역이 안된점이 아쉽지만, 이는 후에 포스트를 업데이트 하겠습니다.
