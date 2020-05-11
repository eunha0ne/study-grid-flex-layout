## 준비하기

### 컨벤션 설정하기

`vue cli`로 프로젝트 생성 후, `prettier`와 `esLint`를 적용했다면 `vue cli`에서 생성한 프로젝트의 코딩 컨벤션이 현재 적용한(prettier, esLint) 컨벤션과 다르기 때문에 `npm run serve`를 실행하면 여러 종류의 프리티어 에러 메시지를 출력하게 되면서 정상적으로 실행되지 않을 수 있다.

프로젝트 전체 파일에 대해서 한번에 오류를 정리하는 방법은 아래의 커맨드를 사용하면 좋다.

```json
"scripts": {
  "prettier:write": "prettier --write \"src/**/*.{js,vue,scss}\""
},
```

### 오류 해결하기

- module' is not defined.eslint no-undef

  `.eslintrc.js` 파일에 아래 내용을 추가해서 `"node": true` 노드 환경임을 선언한다.

  ```json
  "env": {
      "browser": true,
      "amd": true,
      "node": true
  },
  ```
