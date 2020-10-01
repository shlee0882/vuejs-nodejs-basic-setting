## 개요

NodeJs를 이용해 웹서버를 띄우고 VueJs 핵심문법을 확인하는 샘플 프로젝트입니다. 

## 테스트 Deploy URL

https://shlee0882.github.io/vuejs-nodejs-basic-setting

## 설치방법 공유

https://shlee0882.tistory.com/282?category=797808

## vue js 핵심 문법 사용

소스에는 아래 문법이 모두 사용되었으며 테스트 할 수 있게 기능구현되어 있습니다.

- data-bind
- on-click
- props
- components
- data()
- computed
- created()
- methods
- $emit

## 코드 설명 

https://shlee0882.tistory.com/283?category=797808

## 실행하기
```
npm install
npm run serve
```

## GitHub Pages 배포하기

1. gh-pages 설치하기

```
npm install --save gh-pages
```

2. package.json에 추가하기

```
"homepage": "https://shlee0882.github.io/vuejs-nodejs-basic-setting/"


"scripts": {
    "predeploy": "npm run build",
    "deploy": "gh-pages -d dist"
}
```

3. 배포하기
```
npm run deploy
```

4. 배포된 URL 확인하기

```
https://shlee0882.github.io/vuejs-nodejs-basic-setting
```

### 레퍼런스
See [Configuration Reference](https://cli.vuejs.org/config/).
