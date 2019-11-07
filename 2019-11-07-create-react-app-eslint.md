---
title: "[React] create-react-app에서 eject 없이 eslint 사용하기"
category: "React"
date: "2019-11-07 22:22"
---
이번엔 create-react-app의 eject기능 없이 eslint 설정을 바꾸는 방법을 알려드리겠습니다.

# create-react-app 이란?
create-react-app은 리액트 프로젝트를 처음 시작할때 사용하는 프로젝트 시작 커맨드입니다. 대부분의 react 시작하기 관련 글을 읽으시면 이를 이용해 시작하는 것을 볼수있습니다.

이 커맨드를 왜 많이 사용하냐면, react 프로젝트에서 webpack, eslint 등 빌드 툴들에 이 빌드 툴들의 플러그인까지 설정할건 아주 아주 많습니다. 이를 한방에 해결해주는게 create-react-app이며, 이를 이용해 만들어진 프로젝트는 react-scripts라는 커맨드 패키지가 설치되어 여기서 모두 관리해주게됩니다. 그러면서 저희는 오직 리액트 앱 소스코드만 관리하면되는 장점이 있습니다.

## 그럼 무슨 문제가 있나요?
모든 빌드 툴과 플러그인을 관리해주는 만큼 사실 그 설정을 바꾸는 방법은 어렵고 알려지지도 않습니다. 그저 이 react-scripts를 떼어내는 `npm run eject`라는 커맨드로 모든 빌드 툴을 저희 앱 코드에 직접 설치해주는 걸 사용하시는 방법이 많이 알려져있죠.

## 그러면 어떻게 할건데?
최근 2019년 9월 경에 한개의 Pull Request가 creat-react-app의 공식 저장소에 올라왔습니다. ([링크](https://github.com/facebook/create-react-app/pull/7530))

> 참고: create-react-app 패키지 코드내에 [react-scripts 코드](https://github.com/facebook/create-react-app/tree/master/packages/react-scripts)가 같이있습니다.

해당내용은 "`EXTEND_ESLINT` 환경변수를 넣으면, eslint의 설정을 프로젝트의 소스코드에서 가져오기"라는 내용입니다. 딱 저희가 원하던 내용이고, 이미 Merged된 상태입니다.

저희는 대화보다는 코드를 직접 찾아봐 수정사항을 확인합니다. 자세히 보면

![carbon (2)](https://user-images.githubusercontent.com/1689721/68362273-11803f00-016a-11ea-9663-f9064a3c0253.png)

이와같이 `process.env.EXTEND_ESLINT`를 true로 바꿔주면 eslint의 설정 파일을 저희 앱의 소스코드에서 불러오는 것을 확인할 수 있습니다.

## 적용해보자.
이제 적용하기위해 패키지를 설치해야하는데 그냥 `npm install -g create-react-app`을 사용해 최신버전을 설치해준후 react 프로젝트를 생성하시거나, 이미 진행중인 프로젝트에서는 `npm install react-scripts`를 진행해주시면 됩니다.
> 주의: 이미 `npm run eject`를 진행하신 경우는 다시 react-scripts를 붙이는건 굉장히 어렵습니다. 그러니 새로 프로젝트를 생성하는 것을 추천드립니다.

이렇게 패키지를 업데이트 해주시면 적용할 준비는 모두 완료되었습니다.

이제 환경변수를 설정할 차례입니다. 저희는 react-scripts에서 기본으로 제공하는 dotenv를 이용할 예정입니다.
> 참고: [create-react-app의 공식문서 설명 중 dotenv](https://create-react-app.dev/docs/adding-custom-environment-variables/#expanding-environment-variables-in-env)
> package.json에서 react-scripts 실행하는 부분에 환경변수를 추가하셔도 무방합니다.

프로젝트 소스 코드 최상단에 `.env`라는 파일을 만들고 다음과같이 작성합니다.

![carbon (1)](https://user-images.githubusercontent.com/1689721/68362271-104f1200-016a-11ea-8f0c-782d5e744144.png)

이제 이파일은 react-scripts의 dotenv패키지가 로드되면서 저희가 추가한 파일을 찾아 불러오게됩니다. 불러온 환경변수들은 모두 node.js의 기본으로 저장되는 `process.env`라는 곳에 저장하게 됩니다.

이제 eslint를 저희가 설정할 수 있습니다. 그러니 `.eslintrc.json`을 만들어 저희가 사용할 eslint의 설정파일을 만들어줍니다.

![carbon (4)](https://user-images.githubusercontent.com/1689721/68362333-4391a100-016a-11ea-8753-b940baad393e.png)

이제 `npm start`를 실행해보시면 바뀐 eslint설정때문에 오류나 경고가 나올껍니다. 만약에 적용됬는지 잘모르겠으면 rules의 indent를 8로 설정해보세요. 대부분 사람들이 사용하는 코드 들여쓰기가 4칸, 2칸으로 설정되있어서 무조건 오류가 발생해야합니다.

eslint는 코드관리에 아주 중요한 툴입니다. 여기에 prettify에 husky까지 적용하면 여러 사람과 협업할때 각자의 코드스타일이나 사용안하는 변수, import등을 eslint를 이용해 찾아내고, 또한 이런 검사에 CI까지 적용시켜 Pull Request까지 막아버리시면 아주 좋은 코드 관리가 될 수 있겠습니다.
