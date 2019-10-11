---
template: 'BlogPost'
thumb: ''
title: "[C++] Hello World!"
category: "C++"
date: "2018-08-27 23:14"
---
C++은 기존 C언어의 문법에 객체지형의 특성까지 더해져 많은 기능을 지원하는 언어입니다. C언어를 배우셨던 분이라면 좀더 쉽게 배우시거나 때론 내용을 넘겨도 되는 부분도 있습니다.

또한 C언어의 작업환경과 동일하게 하셔도 되며, Visual Studio와 같은 IDE에서 작업하시면 됩니다. 본 강좌는 IDE를 보여주진않고 오직 코드로만 설명합니다.

C++파일은 확장자가 cpp이며, 아래 내용은 모든 프로그래밍 언어의 기초인 Hello, World! 출력 프로그램입니다.

### 코드
<img src="https://user-images.githubusercontent.com/1689721/66671978-2c10e680-ec98-11e9-91ba-31bd52566922.png" alt="code">

### 출력 내용
```
Hello World
```

### 설명
```cpp
#include <iostream>
using namespace std;
```
C++ 기본 API 라이브러리중 iostream을 가져오고, 그중 std(standard 줄임말)라는 네임스페이스를 사용하겠다고 호출했습니다.
네임스페이스는 추후 자세히 다루도록하겠습니다.

```cpp
int main() {
  ...
  return 0;
}
```
프로그램의 제일 처음 실행하는 함수를 정의합니다. 이때 함수의 이름은 `main`이여야만 하며, 이는 프로그램의 규칙입니다.

`return` 키워드는 함수의 종료를 의미하며, 뒤에오는 변수는 해당 함수가 호출된 곳으로 되돌려줍니다. (main에서의 return은 프로그램 종료 상태를 의미하며, 0은 정상종료를 뜻합니다.)

```cpp
cout << "Hello World" << endl;
```
`iostream의 std`안에 있는 `cout`과 `endl`입니다. 각각 Console Out / End Line의 줄임말입니다.

<<연산자는 우측에서 좌측으로 연산됩니다. 그러므로, `"Hello World"`라는 문자열에 End Line을 붙여 Hello World 다음에 줄넘김을 표시합니다.
그렇게 만들어진 문자열을 Console Out으로 넘겨줍니다. 이는 콘솔 출력을 의미합니다.
