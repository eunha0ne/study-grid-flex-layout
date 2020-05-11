## 준비하기

### 컨벤션 설정하기

`vue cli`로 프로젝트 생성 후, `prettier`와 `esLint`를 적용했다면 `vue cli`에서 생성한 프로젝트의 코딩 컨벤션이 현재 적용한(prettier, esLint) 컨벤션과 다르기 때문에 `npm run serve`를 실행하면 여러 종류의 프리티어 에러 메시지를 출력하게 되면서 정상적으로 실행되지 않을 수 있다.

프로젝트 전체 파일에 대해서 한번에 오류를 정리하는 방법은 아래의 커맨드를 사용하면 좋다.

```json
"scripts": {
  "prettier:write": "prettier --write \"src/**/*.{js,vue,scss}\""
},
```

## 노트

`grid`는 2차원 레이아웃 시스템을 바탕으로 한다. 그리드 컨테이너에서 하위 아이템에 대한 스타일 표현을 정의할 수 있다.

```scss
.container {
  &--grid {
    display: grid;
    grid-template-columns: repeat(5, 250px);
    grid-template-rows: 150px;
    gird-gap: 30px;
  }
}
```

`flex`는 일차원 레이아웃 시스템을 바탕으로 한다. 위에서 작성한 스타일을 외관적으로 동일하게 하려면 아래와 같다. 플랙스 컨테이너에 영향을 받는 플렉스 아이템은 자신을 표현할 때 3가지 세부 상태를 통해 정의할 수 있다.

- flex-grow: 자신이 차지할 공간의 정도를 결정. 기본값은 `0`이다. 소수점이나 양의 정수로 증감을 표현할 수 있다. 예를 들어 0.1 또는 2 처럼 선언
- flex-shrink: 컨테이너 크기에 맞추어 자신을 축소할지를 결정 (0: 축소하지 않음, 1: 축소함)
- flex-basis: 플렉스 아이템의 기본 크기를 정의. 컨테이너에서 정의된 `flex-direction` 속성에 따라 높이와 너비로 나타낸다.

축약해서 `flex: flex-grow | flex-shrink | flex-basis`와 같이 선언할 수 있다.

```scss
.container {
  &--flex {
    display: flex;
    flex-flow: row nowrap;
  }
}

.item {
  margin: 0 (30px / 2);
  flex: 0 0 250px;
  width: 250px;
  height: 150px;

  &:first-of-type {
    margin-left: 0;
  }

  &:last-of-type {
    margin-right: 0;
  }
}
```

## 오류 해결하기

- **module' is not defined.eslint no-undef**

  `.eslintrc.js` 파일에 아래 내용을 추가해서 `"node": true` 노드 환경임을 선언한다.

  ```json
  "env": {
      "browser": true,
      "amd": true,
      "node": true
  },
  ```

- **scss 컴파일하기**

  ```
  npm install -D sass-loader sass
  ```

  sass 문법과 scss 문법을 잘 가려서 스타일 태그에 선언한다.

  ```html
  <style lang="scss" scoped>
    /* ... */
  </style>
  ```

- **에디터에서 줄바꿈을 오류로 인식 한다면**

  VSCode 에디터 오른쪽 하단의 `CRLF`를 `LF` 형태로 바꿔준다.

  > 그런데 애초에 무엇이 이런 문제를 갑자기 발생시켰을까? 코드 포맷팅?

  - CR: Carriage Return
  - LF: Line Feed

## Reference

- [Read: understanding-css-grid](https://medium.com/sketch-app-sources/understanding-css-grid-ce92b7aa67cb)
- [Read: 이번에야말로 CSS Grid를 익혀보자](https://studiomeal.com/archives/533)
- [Link: grid-examples](https://gridbyexample.com/examples/)
