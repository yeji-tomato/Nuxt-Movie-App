# nuxt-movie-app
검색 엔진 최적화로 동적인 페이지들의 메타 정보를 openGraph를 활용해서 작성 

## Deployment
[https://nuxt-movie-yeji.herokuapp.com <br>
![화면 캡처 2021-08-11 150345](https://user-images.githubusercontent.com/59958929/128977910-0579ec50-7a88-4cf9-bfb6-a49e7504da9c.png)](https://nuxt-movie-yeji.herokuapp.com/)

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

## Build Setup

```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm run start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, check out the [documentation](https://nuxtjs.org).

## Special Directories

You can create the following extra directories, some of which have special behaviors. Only `pages` is required; you can delete them if you don't want to use their functionality.

### `assets`

The assets directory contains your uncompiled assets such as Stylus or Sass files, images, or fonts.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/assets).

### `components`

The components directory contains your Vue.js components. Components make up the different parts of your page and can be reused and imported into your pages, layouts and even other components.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/components).

### `layouts`

Layouts are a great help when you want to change the look and feel of your Nuxt app, whether you want to include a sidebar or have distinct layouts for mobile and desktop.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/layouts).


### `pages`

This directory contains your application views and routes. Nuxt will read all the `*.vue` files inside this directory and setup Vue Router automatically.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/get-started/routing).

### `plugins`

The plugins directory contains JavaScript plugins that you want to run before instantiating the root Vue.js Application. This is the place to add Vue plugins and to inject functions or constants. Every time you need to use `Vue.use()`, you should create a file in `plugins/` and add its path to plugins in `nuxt.config.js`.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/plugins).

### `static`

This directory contains your static files. Each file inside this directory is mapped to `/`.

Example: `/static/robots.txt` is mapped as `/robots.txt`.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/static).

### `store`

This directory contains your Vuex store files. Creating a file in this directory automatically activates Vuex.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/store).
