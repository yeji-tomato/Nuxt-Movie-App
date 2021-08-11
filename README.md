# nuxt-movie-app
검색 엔진 최적화로 동적인 페이지들의 메타 정보를 openGraph를 활용해서 작성 

## Deployment
[https://nuxt-movie-yeji.herokuapp.com <br>
![image](https://user-images.githubusercontent.com/59958929/128978376-c2544a8e-5c53-4e08-95be-202bdd140710.png)](https://nuxt-movie-yeji.herokuapp.com/)

## SPA   vs SSR

SPA → Single Page Application 

장점 : 최초로 응답받은 서버를 기반으로 해서 다른 페이지도 구분해줌

페이지가 바뀌더라도 서버에 해당 페이지에 대한 새로운 요청이 전송되거나 응답받는 개념이 아님

단점 : SEO 페이지가 많거나 검색 기능을 제대로 수행할 수 없음

그래서 서버사이드 렌더링을 이용함

(CSR → Client Side Rendering) ⇒ SPA보다 큰 개념

SSR → Server Side Rendering

서버 측에서 페이지를 만들어서 내보내주는 것

[Nuxt.js - Vue.js 프레임워크](https://ko.nuxtjs.org/)

`Nuxt는 vue2에서만 적용되므로 vue2의 문법으로 작성해주어야 한다.`


### import

```jsx
additionalData: '@import "~/scss/main";'
```

webpack에선 따로 패키지 처리 없이 webpack.config.js에 작성이 가능했지만 Nuxt에선 따로 패키지를 설치해야한다!

```
$ npm i -D @nuxtjs/style-resources
```

**`nuxt.config.js`**

```jsx
modules: [
    '@nuxtjs/style-resources'
  ],

  styleResources: {
    scss: [
      '~/scss/main.scss'
    ]
  },
```

### Store 폴더

Nuxt에선 Store라는 기본 개념이 존재하기 때문에 

**`index.js`** 

→ module로 movie와 about을 등록해줌

```jsx
import Vue from 'vue'
import Vuex from 'vuex'
import movie from './movie'
import about from './about'

Vue.use(Vuex)

export default new Vuex.Store({
  modules: {
    movie,
    about
  }
})
```

vue에서 작성했던 index.js의 내용은 삭제해주어야 한다.

⇒ 충돌이 발생할 수 있기 때문에 

**단. index.js파일은 삭제하면 안됨!!!** 

**→ index.js파일이 존재하게 되면 그 때 내부적으로 store를 활성화할 수 있는 기능을 가지고 있기 때문에!!!**

### Babel / postcss

vue에서는 babelrc라는 js파일을 제공해서 기본적인 구성을 했지만 Nuxt에서는 nuxt.config.js파일에다가 명시하도록 만들어져 있음

```jsx
build: {
    babel: {
      presets: ['@babel/preset-env'],
      plugins: [
        ['@babel/plugin-transform-runtime']
      ]
    },
    postcss: {
      plugins: [
        require('autoprefixer')
      ]
    }
  }
```

⚠️ **주의할 점!**

jest의 단위테스트에서 원래는 babelrc를 이용해 코드를 변환해서 사용했기에 문제가 발생

→ jest단위테스트를 위해서 .babelrc.js를 root경로에 넣어주어야 함

### express

```
$ npm i -D express 
```

### APIKEY

```
$ npm i -D @nuxtjs/dotenv
```
