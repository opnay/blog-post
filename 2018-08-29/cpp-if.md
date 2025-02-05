---
template: 'BlogPost'
thumb: ''
title: "[C++] 조건문 알아보기"
category: "C++"
date: "2018-08-29 00:41"
---
조건문은 `만약 ~이면 ~을 한다`라는 의미를 지닌 문법이고, 이 조건문이란건 앞으로 코딩을 하면서 많이 쓰이게되는 문법중 하나입니다.

C++에서의 조건문은 if, switch가 있으며, 이 문법들은 모두 C언어에서 사용되던 것들과 동일합니다.

## IF 예제
{% include services/gist.html src="dab3805902f319d9caf5505211095611" %}

## IF 결과
```
A와 B는 다릅니다.
B는 0보다 큽니다.
```

## IF 설명
- 1~4: 이전 "[[C++] Hello World!](/c++/201808-cpp-helloworld)" 게시물에서 설명을 했습니다.
- 5~6: int형 변수 A와 B를 선언했고 A는 0, B는 1을 초기값으로 넣어줬습니다.
- 8: if문의 기본 형태는 `if(조건문) {실행할 내용}`이고, 그 형태 그대로 작성되었습니다. `조건문`이 참(true)일 경우 바로 다음에오는 `{ }`의 내용을 실행하게됩니다.
- 10: if문과 함께 사용할 수 있는 else문 입니다. if의 조건문이 거짓(false)일 경우 else의 내용을 실행하게됩니다.
<br>현재 A와 B는 같지 않으므로 else의 내용을 실행하게되어 `A와 B는 다릅니다.`가 출력된것입니다.
- 16: else문에 바로 if문을 쓰면 또 하나의 조건문을 추가로 넣을 수 있습니다.
<br>14번 줄에서 `A > 0`을 확인했지만 결과는 거짓이라 15번 줄을 건너띄고 16번줄을 실행하게됩니다. 여기서는 `B > 0`의 결과는 참이므로 17번줄을 실행하고 18번의 else문을 건너띄게됩니다.

---

## Switch 예제
{% include services/gist.html src="0f89cf43c31dd798ddf76eaa50b1efb1" %}

## Switch 결과
```
A는 0입니다.
```

## Switch 설명
- 5: int형 변수 A를 선언하며, 초기값으로 0을 넣어줬습니다.
- 7~17: 전체적인 switch문의 형태입니다.
- 7: switch문에서 비교할 변수를 A로 설졍했습니다.
- 8: switch문에서 필수적인 `case 정수:`입니다. 7번줄에서 설정한 A라는 변수가 `case 0:` 즉, 0일때 아래의 9번줄을 실행하게 됩니다.
<br>if문과 비교를 하면 `if (A == 0)`에 해당되는 부분입니다.
- 10: `break;`는 switch에서 중요합니다. 현재 블럭(`{ }`)에 해당되는 switch문을 빠져나오게 해주는 키워드입니다. 만약 이 키워드가 없으면 switch문이 끝나거나 다른 조건에 작성해 놓은 `break;`를 만날때까지 모든 내용을 실행하게 됩니다.
- 11~13: 위의 8~10번과 동일합니다. A가 1일때 12번줄부터 실행하게 됩니다.
- 14: `default`라는 값은 위에 작성한 `case`에 해당되는게 아무것도 없을 경우를 얘기합니다. if문으로 치자면 `else`에 해당되는 부분입니다.
- 16: switch문의 끝이라 `break`는 사실상 없어도 무관합니다.
