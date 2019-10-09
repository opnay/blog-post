---
template: 'BlogPost'
thumb: "https://user-images.githubusercontent.com/1689721/66471455-4a26ed00-eac6-11e9-92ed-2d4e5d716a74.png"
title: "Kotlin 콘솔에서 입력받는 3가지 방법"
category: "Kotlin"
date: "2018-10-06 00:45"
---
<p style="text-align:center;"><img src="https://user-images.githubusercontent.com/1689721/66471415-3a0f0d80-eac6-11e9-8e7b-5c6ebbc39f09.png" alt="Kotlin" style="height:150px;"></p>

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
