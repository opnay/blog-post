---
title: "[Kotlin] HelloWorld"
category: "Kotlin"
date: "2018-10-05 01:57"
image: "/assets/thumb/kotlin.svg"
---
<p style="text-align:center;"><img src="{{ site.url }}/assets/kotlin/kotlin.svg" alt="Kotlin" style="height:150px;"></p>

Kotlin이란 언어는 IntelliJ IDEA라는 개발환경을 만든 Jetbrain에서 고안한 언어이고, 그 종류는 JVM / JS / Native 세종류로 나눠집니다. Native는 네이티브 실행파일(Windows, Linux, OSX 실행파일, .so라이브러리 등)이며, JS는 JavaScript로, JVM은 Java언어로 컴파일됩니다.

## Kotlin JVM
JVM은 Java Virtual Machine의 약자이며, Java언어를 사용할때 배울수 있는 가상머신의 일종입니다. (여기서는 간단한 과정만 설명하겠습니다.)

Java라는 언어는 어떤 운영체제, CPU든 종류에 따지지 않고 사용할 수 있는 프로그래밍 언어입니다. 하지만 이런 Java를 있게한건 JVM이고, 이 JVM은 각 운영체제, CPU별로 배포가 되어있는 상태입니다. 그런 JVM위에서 돌아가는 것이 Java이고, 이를 통해 운영체제, CPU와 자유로운 프로그래밍이 가능해집니다.

Kotlin JVM은 이 JVM에서 실행할 수 있는 바이트코드인 .class파일로 컴파일 하는 과정이있고 중간에 Java언어로 한번 변환이 됩니다.

전체적인 과정은 .kt(Kotlin) -> .java(Java) -> .class(바이트코드) 순으로 컴파일됩니다. (JVM종류에 따라서 .class가 아닌 다른 파일로 추가변환과정이 있을 수 있습니다.)

제가 이 내용을 넣은 이유가 Kotlin Android를 하게되면 Kotlin 기본제공 함수들이나 AndroidX함수들을 남발하게되는데 실제 .java로 컴파일되는 과정을 보게되면, Java언어로 무겁게 구현된 메소드를 사용한 Kotlin함수가 존재하며, 이를 과도하게 사용해 실제 앱의 성능을 떨어트리는 결과를 초래할 수 있습니다. 따라서 성능에 문제가 생기거나하는 이유가 발생할 수 있으니, 웬만해서는 Java언어도 참고하시는게 좋습니다.

제가 할 강좌는 Kotlin JVM이며, 이는 Kotlin Android에서도 사용가능한 함수 / 메소드를 다뤄볼 예정입니다.

## Hello World!
이번 강좌는 언제나 어떤 언어든간에 처음시작하게되는 Hello World출력 프로그램입니다.

실제 개발환경은 Intellij IDEA를 추천드리며, [이곳](https://www.jetbrains.com/idea/download/)을 통해 무료인 Community버전을 다운받으실 수 있습니다.

{% include services/gist.html src="57147d1d80198b004a12c18f4bda2a42" %}


```
Hello World!
```

1번줄: Kotlin의 메인함수입니다. Kotlin으로 만든 프로그램은 모두 여기 main함수에서 시작됩니다.

2번줄: println이라는 Kotlin기본 함수를 통해 출력합니다. 해당 함수는 Java의 System.out.println 메소드를 실행하게 되어있습니다.

> - [Wikipedia - JVM](https://ko.wikipedia.org/wiki/%EC%9E%90%EB%B0%94_%EA%B0%80%EC%83%81_%EB%A8%B8%EC%8B%A0)
> - [Wikipedia - 바이트코드](https://ko.wikipedia.org/wiki/%EC%9E%90%EB%B0%94_%EB%B0%94%EC%9D%B4%ED%8A%B8%EC%BD%94%EB%93%9C)
