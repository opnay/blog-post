---
template: 'BlogPost'
thumb: "data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzAwIiBoZWlnaHQ9IjMwMCIgdmlld0JveD0iMCAwIDMwMCAzMDAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxyZWN0IHdpZHRoPSI3NTAiIGhlaWdodD0iMzAwIiBmaWxsPSJ3aGl0ZSIvPgo8bWFzayBpZD0ibWFzazAiIG1hc2stdHlwZT0iYWxwaGEiIG1hc2tVbml0cz0idXNlclNwYWNlT25Vc2UiIHg9IjAiIHk9IjAiIHdpZHRoPSIzMDAiIGhlaWdodD0iMzAwIj4KPHJlY3Qgd2lkdGg9IjMwMCIgaGVpZ2h0PSIzMDAiIGZpbGw9IiNDNEM0QzQiLz4KPC9tYXNrPgo8ZyBtYXNrPSJ1cmwoI21hc2swKSI+CjxyZWN0IHdpZHRoPSI3NTAiIGhlaWdodD0iMzAwIiBmaWxsPSJ1cmwoI3BhaW50MF9saW5lYXIpIi8+CjxwYXRoIGQ9Ik0xNTAgOTBIOTBWMTUwTDE1MCA5MFoiIGZpbGw9InVybCgjcGFpbnQxX2xpbmVhcikiLz4KPHBhdGggZD0iTTkwIDE1MEwxNTAgOTBIMjEwTDkwIDIxMFYxNTBaIiBmaWxsPSJ1cmwoI3BhaW50Ml9saW5lYXIpIi8+CjxwYXRoIGQ9Ik0xNTAgMTUwTDkwIDIxMEgyMTBMMTUwIDE1MFoiIGZpbGw9InVybCgjcGFpbnQzX2xpbmVhcikiLz4KPC9nPgo8ZGVmcz4KPGxpbmVhckdyYWRpZW50IGlkPSJwYWludDBfbGluZWFyIiB4MT0iMjk5IiB5MT0iLTUuMzE2NzNlLTA2IiB4Mj0iMi44Mjc0OGUtMDUiIHkyPSIzMDAiIGdyYWRpZW50VW5pdHM9InVzZXJTcGFjZU9uVXNlIj4KPHN0b3Agc3RvcC1jb2xvcj0iIzU4Q0ZGQiIvPgo8c3RvcCBvZmZzZXQ9IjEiIHN0b3AtY29sb3I9IiNGMEZGMDAiLz4KPC9saW5lYXJHcmFkaWVudD4KPGxpbmVhckdyYWRpZW50IGlkPSJwYWludDFfbGluZWFyIiB4MT0iMTYzLjIiIHkxPSI3Ni44IiB4Mj0iOTAiIHkyPSIxNTAiIGdyYWRpZW50VW5pdHM9InVzZXJTcGFjZU9uVXNlIj4KPHN0b3Agc3RvcC1jb2xvcj0iI0ZGNkZEOCIvPgo8c3RvcCBvZmZzZXQ9IjAuNTE5MzM3IiBzdG9wLWNvbG9yPSIjM0M4Q0U3Ii8+CjxzdG9wIG9mZnNldD0iMSIgc3RvcC1jb2xvcj0iIzAwRUFGRiIvPgo8L2xpbmVhckdyYWRpZW50Pgo8bGluZWFyR3JhZGllbnQgaWQ9InBhaW50Ml9saW5lYXIiIHgxPSIxNTAiIHkxPSI5MCIgeDI9IjkwIiB5Mj0iMTUwIiBncmFkaWVudFVuaXRzPSJ1c2VyU3BhY2VPblVzZSI+CjxzdG9wIHN0b3AtY29sb3I9IiNGQjg1NDUiLz4KPHN0b3Agb2Zmc2V0PSIxIiBzdG9wLWNvbG9yPSIjRkY2RkQ4Ii8+CjwvbGluZWFyR3JhZGllbnQ+CjxsaW5lYXJHcmFkaWVudCBpZD0icGFpbnQzX2xpbmVhciIgeDE9IjE2MC44IiB5MT0iMTM5LjIiIHgyPSI5MCIgeTI9IjIxMCIgZ3JhZGllbnRVbml0cz0idXNlclNwYWNlT25Vc2UiPgo8c3RvcCBzdG9wLWNvbG9yPSIjRkY2RkQ4Ii8+CjxzdG9wIG9mZnNldD0iMC4zMzYwMiIgc3RvcC1jb2xvcj0iIzNDOENFNyIvPgo8c3RvcCBvZmZzZXQ9IjEiIHN0b3AtY29sb3I9IiMwMEVBRkYiLz4KPC9saW5lYXJHcmFkaWVudD4KPC9kZWZzPgo8L3N2Zz4K"
title: "Kotlin 콘솔에서 입력받는 3가지 방법"
category: "Kotlin"
date: "2018-10-06 00:45"
---
<p style="text-align:center;"><img src="{{ site.url }}/assets/kotlin/kotlin.svg" alt="Kotlin" style="height:150px;"></p>

Kotlin이란 언어는 Java의 클래스, 메소드가 대부분 사용이 가능한 언어입니다. 그런 Kotlin언어의 콘솔 프로그램에서 입력을 받는 방법 3가지를 소개하겠습니다.

## 1. readLine
Kotlin 기본 함수중에는 `readLine()`이라는 함수가 있습니다. 이 함수는 콘솔창에서 입력이되면, 줄개행(엔터)를 기준으로 한줄씩 읽게되는 함수입니다.

이 함수의 리턴 타입은 `String?`이며, `?`가 붙은 Nullable 타입입니다. 즉, 입력을 받을때 Null이 올 수 있는 함수입니다.

{% include services/gist.html src="6ef205180759c78aa60789b805ac6f75" %}

입력
```
12345abc
```

출력
```
12345abc
```

2번줄: `!!`을 붙여 Not Null타입으로 변환해줬습니다.

3번줄: `readLine()!!`을 통해 읽어들인 한줄을 그대로 `println`을 통해 출력합니다.

## 2. Scanner
Java에서 사용하던 Scanner라는 클래스입니다. Kotlin에서는 Java의 클래스와 메소드를 전부 사용가능합니다.

{% include services/gist.html src="26e9a1e1c352113df6791e63b15d84d0" %}

입력
```
1234
```

출력
```
1234
```

1번줄: Java의 Scanner클래스를 사용하기 위해 `import`키워드를 사용해 가져왔습니다.

4번줄: Scanner객체를 생성합니다. `` System.`in` ``은 Kotlin의 `in`이라는 키워드가 겹쳐 `` `in` ``으로 사용합니다.

5번줄: 만들어진 객체를 이용해 정수를 읽어들입니다.

6번줄: 읽어들인 정수를 출력합니다.

## 3. BufferedReader
이 또한 Java에서 사용하던 클래스입니다. Scanner를 이용하는 것보다 빠르니 알고리즘 풀이할때 많이 쓰이고, 기타 파일 입출력, 리눅스 또는 OSX에서 파이프 실행등에서 많이 쓰입니다.

{% include services/gist.html src="df0c232c8a3caf066799425200da47c5" %}

입력
```
가나다라마바사
1234567
abcdEFGH
```

출력
```
가나다라마바사
1234567
abcdEFGH
```

1번줄: BufferedReader 클래스를 가져옵니다.

4번줄: 객체를 생성합니다. 생성자의 매개변수는 `Reader`클래스 객체가 필요하므로 ``System.`in`.reader()``를 사용합니다.

6번줄: 4번줄에서 생성한 객체를 이용해 Kotlin확장 함수인 `forEachLine`이라는 람다식 함수를 사용합니다. 이 함수로 입력받은 버퍼의 각 줄별로 람다식을 실행하게됩니다. 따라서 각줄의 내용을 `println`을 통해 출력하는 내용입니다.

※ Kotlin의 람다식에서 매개변수가 1개이고, 별다른 별칭을 지정안해주면 매개변수의 이름은 기본적으로 it으로 설정됩니다.

---

Java클래스가 사용이 가능하다는 점으로 위에 설명한 3가지 방법 말고 다른 방법의 키입력, 버퍼읽기등이 있습니다. 제가 아직 모르는 내용의 함수도 있고, 설명이 미흡하기도 합니다. 언제든지 댓글로 추가적인 내용이나 오타, 수정 등의 지적을 해주시면 감사합니다.
