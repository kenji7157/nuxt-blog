# kk-nuxt-blog

## プロジェクト作成時の初期設定
```
-> % create-nuxt-app kk-nuxt-blog

create-nuxt-app v3.4.0
✨  Generating Nuxt.js project in kk-nuxt-blog
? Project name: kk-nuxt-blog
? Programming language: TypeScript
? Package manager: Npm
? UI framework: Vuetify.js
? Nuxt.js modules: (Press <space> to select, <a> to toggle all, <i> to invert selection)
? Linting tools: ESLint, Prettier, Lint staged files
? Testing framework: Jest
? Rendering mode: Universal (SSR / SSG)
? Deployment target: Static (Static/JAMStack hosting)
? Development tools: jsconfig.json (Recommended for VS Code if you're not using typescript)
? Continuous integration: None
? Version control system: Git
```

## micro cmsの登録
参考記事：https://microcms.io/blog/microcms-nuxt-jamstack-blog/
- 開発メアドで登録
- サービス名：kk-nuxt-blog
- APIの型：リスト形式
- APIスキーマ定義
   - title/タイトル/テキストフィールド
   - body/本文/リッチエディタ
- API叩くときはaxiosモジュールを利用

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

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).
