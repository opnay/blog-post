---
template: 'BlogPost'
thumb: "https://user-images.githubusercontent.com/1689721/66471455-4a26ed00-eac6-11e9-92ed-2d4e5d716a74.png"
title: "Kotlin 확장 함수 활용하기"
category: "Kotlin"
date: "2018-11-04 20:47"
image: "/assets/thumb/kotlin.svg"
---
<p style="text-align:center;"><img src="https://user-images.githubusercontent.com/1689721/66471415-3a0f0d80-eac6-11e9-8e7b-5c6ebbc39f09.png" alt="Kotlin" style="height:150px;"></p>

Kotlin 언어를 사용하다보면 이런 구문이 자주 보이게 될겁니다. `T.apply {}`, `T.run {}` 등 Java에는 없지만 Kotlin에 존재하는 확장함수라는 것을 직접 만들어보도록 하겠습니다.

## 확장함수(Extension Function)
Java에서 기본으로 제공되는 클래스들에 함수를 추가하려면 새로운 클래스를 만들거나 static함수를 만들어 사용해야만하는 불편함이 있었습니다.

간단한 예를 들기위해 boolean과 int간의 형변환 예제를 만들어 보겠습니다.

{% include services/gist.html src="624d15c72cfb91d1382d9048508663ee" %}

삼항연산자로 짧은 코드를 만들었지만, 한눈에 의미를 파악하기 어렵고, 이런 코드가 반복되다보면 그렇게 보기좋은 코드가 되지 못합니다.

그래서 별도의 사용자 클래스내의 static타입의 함수를 만들어 사용하기도 했습니다. (어디까지나 설명을 위해 만든 예제이고, 실제로 이런식으로 bool과 int간의 형변환을 자주 사용하진 않습니다.)

하지만 Kotlin에서는 확장함수를 통해 Int와 Boolean 클래스에 함수를 만들어줘 클래스를 만드는 번거로움이 없이 편하게 함수를 추가할 수 있습니다.

{% include services/gist.html src="4ff1dd8b88d7670028a9138d0be22b1c" %}

Int와 Boolean클래스에 확장함수를 만들어 주어 기존 클래스에 있는 것처럼 사용할 수 있습니다.

참고로 이렇게 확장함수를 넣어주게되면 `100.toBoolean()`, `true.toInt()` 이런식의 코드 또한 가능합니다.

## 람다식(Lambda Expression)
Kotlin의 람다식은 변수처럼 활용이 가능합니다. 특정 함수내에서만 존재하는 함수를 만들거나, 상황에 따라 함수의 내용이 수정되어야 할때 아주 유용한 방법입니다.

람다식을 매개변수로하는 함수 하나를 만들어 보겠습니다.

{% include services/gist.html src="c082d9001a753da7646adf0fadc0828c" %}

Int 클래스에 returnMe라는 함수를 하나 만들었습니다. 이 함수는 약간 복잡해 보이지만 천천히 보시면 이해할 수 있습니다.

먼저 매개변수인 some을 보겠습니다. `() -> String`으로 String을 리턴하는 람다식입니다. 하지만 `Int.()`으로 시작하는 걸보면 이 람다식은 Int의 확장 함수로 사용됩니다. 따라서 `returnMe`라는 함수 내에서는 Int클래스에는 some이라는 함수를 사용할 수 있습니다.

함수의 내용을 보시면 `= this.some()`이 오는데 현재 `returnMe`라는 함수는 Int클래스의 확장 함수이므로 this는 Int형 객체가 됩니다. 그러니 `some()`이라는 확장 함수가 사용할 수 있는 것이죠. 그 리턴값은 String형으로 `returnMe` 함수의 리턴값으로 다시 넘겨지게됩니다.

마지막으로 사용하는 4~5라인을 보시면 아시겠지만, Kotlin의 함수에서 마지막 매개변수가 람다식이면 이는 `()`에서 생략이 가능해집니다. 최종적으로는 `T.apply {}`와 같은 형태가 되는것이죠.

---

Kotlin의 확장 함수뿐만 아니라 람다식과 함께 쓰인다면 좀더 좋은 시너지 효과를 낼 수 있습니다.

물론 예제처럼 굳이 사용할 필요가 없는 곳에서 사용해 남용하게되면 이는 좋지 못한 코드가 되겠지만 그 부분은 이 글을 읽으시는 분이 직접 판단하셔야 할 부분입니다.

---

오타, 오류 등이 있다면 댓글이나 이메일을 통해 알려주시면 감사하겠습니다. :D