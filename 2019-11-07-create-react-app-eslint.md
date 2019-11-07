---
title: "[React] create-react-app에서 eject 없이 eslint 사용하기"
category: "React"
date: "2019-11-07 22:22"
---
create-react-app의 eject기능 없이 eslint 설정을 바꾸는 방법을 알려드리겠습니다.

리액트를 처음 시작할때 create-react-app을 이용해 만들게됩니다.
이 create-react-app을 이용해 만들면 react-scripts라는 패키지를 통해 빌드 / 개발용 서버를 사용할 수 있도록 커맨드를 제공해줍니다.
이 react-scripts안에 webpack, eslint, babel등 각종 빌드용 패키기들의 설정이 저장되어있는데 이 설정을 수정하는 방법을 모르시는 분들이 꽤 많더라구요.

그래서 react-scripts 공식 패키지를 뜯어서 직접찾아 이 빌드용 패키지들중 하나인 eslint를 직접 설정할 수 있도록 하는 방법을 알려드리겠습니다.

먼저 react-scripts의 [공식 저장소](https://github.com/facebook/create-react-app/tree/master/packages/react-scripts)에서 패키지 소스 코드를 보게되면, `config/webpack.config.js`파일의 356번라인쯤을 보시면 webpack의 eslint 플러그인 설정이있습니다.
그 내용을 자세히 보면

![carbon (2)](https://user-images.githubusercontent.com/1689721/68361835-9d916700-0168-11ea-9616-5efa8d1f1355.png)

이와같이 `process.env.EXTEND_ESLINT`를 true로 바꿔주면 eslint의 설정 파일을 저희 앱의 소스코드에서 불러오는 것을 확인할 수 있습니다.

이제 저 값을 true로 바꿔줄건데 저건 react-scripts실행시 환경변수로 추가를 해줘야합니다. 그러나 모든 react-scripts 커맨드에 EXTEND_ESLINT를 추가해줄수는 없으니 저희는 dotenv라는 패키지를 이용할겁니다.

본인의 앱 소스 코드 최상단에 `.env`라는 파일을 만들고 다음과같이 작성합니다.

![carbon (1)](https://user-images.githubusercontent.com/1689721/68359254-ae3cdf80-015e-11ea-949d-1db1e4224a92.png)

이제 이파일은 react-scripts 커맨드상의 설정때문에 dotenv패키지가 로드되고, `.env`라는 파일을 찾아 불러오게됩니다. 불러온 환경변수들은 모두 node.js의 기본으로 저장되는 `process.env`라는 곳에 저장하게 됩니다.

이제 eslint를 저희가 설정할 수 있습니다. 그러니 `.eslintrc.json`을 만들어 저희가 사용할 eslint의 설정파일을 만들어줍니다.
