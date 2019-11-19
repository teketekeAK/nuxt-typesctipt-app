# nuxt-app-with-ts

> My top-notch Nuxt.js project

## Build Setup

``` bash
# install dependencies
$ yarn install

# serve with hot reload at localhost:3000
$ yarn dev

# build for production and launch server
$ yarn build
$ yarn start

# generate static project
$ yarn generate
```

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).


## 
### nuxt version up
```
$ yarn add nuxt

yarn add v1.19.1
[1/4] 🔍  Resolving packages...
[2/4] 🚚  Fetching packages...
[3/4] 🔗  Linking dependencies...
[4/4] 🔨  Building fresh packages...
success Saved lockfile.
success Saved 1 new dependency.
info Direct dependencies
└─ nuxt@2.10.2
info All dependencies
└─ nuxt@2.10.2
✨  Done in 4.95s.
```

### typescript-build install
```
$ yarn add --dev @nuxt/typescript-build

yarn add v1.19.1
[1/4] 🔍  Resolving packages...
[2/4] 🚚  Fetching packages...
[3/4] 🔗  Linking dependencies...
[4/4] 🔨  Building fresh packages...
success Saved lockfile.
success Saved 32 new dependencies.
info Direct dependencies
└─ @nuxt/typescript-build@0.3.4
info All dependencies
├─ @nuxt/types@0.3.4
├─ @nuxt/typescript-build@0.3.4
├─ @types/anymatch@1.3.1
├─ @types/babel__core@7.1.3
├─ @types/babel__generator@7.6.0
├─ @types/babel__template@7.0.2
├─ @types/babel__traverse@7.0.7
├─ @types/body-parser@1.17.1
├─ @types/clean-css@4.2.1
├─ @types/compression@1.0.1
├─ @types/etag@1.8.0
├─ @types/express@4.17.2
├─ @types/html-minifier@3.5.3
├─ @types/memory-fs@0.3.2
├─ @types/mime@2.0.1
├─ @types/optimize-css-assets-webpack-plugin@5.0.1
├─ @types/range-parser@1.2.3
├─ @types/relateurl@0.2.28
├─ @types/serve-static@1.13.3
├─ @types/source-list-map@0.1.2
├─ @types/tapable@1.0.4
├─ @types/terser-webpack-plugin@2.2.0
├─ @types/webpack-bundle-analyzer@2.13.3
├─ @types/webpack-dev-middleware@2.0.3
├─ @types/webpack-hot-middleware@2.16.5
├─ @types/webpack-sources@0.1.5
├─ fork-ts-checker-webpack-plugin@3.1.0
├─ loglevel@1.6.6
├─ microevent.ts@0.1.1
├─ ts-loader@6.2.1
├─ typescript@3.6.4
└─ worker-rpc@0.1.1
✨  Done in 6.62s.
```

### add typescript-build

nuxt.config.js

```js
  // ... 略
  buildModules: [
    '@nuxt/typescript-build', // これを追加
  ]
  // ... 略
```

### create tsconfig.json

```
$ touch tsconfig.json
```

### add typescript-build
```
$ yarn add @nuxt/typescript-runtime

yarn add v1.19.1
[1/4] 🔍  Resolving packages...
[2/4] 🚚  Fetching packages...
[3/4] 🔗  Linking dependencies...
[4/4] 🔨  Building fresh packages...

success Saved lockfile.
success Saved 6 new dependencies.
info Direct dependencies
└─ @nuxt/typescript-runtime@0.2.4
info All dependencies
├─ @nuxt/typescript-runtime@0.2.4
├─ arg@4.1.1
├─ diff@4.0.1
├─ make-error@1.3.5
├─ ts-node@8.5.2
└─ yn@3.1.1
✨  Done in 2.59s.

```

### change package.json

scriptsの中を下記のように更新
```
  "scripts": {
    "dev": "nuxt-ts",
    "build": "nuxt-ts build",
    "generate": "nuxt-ts generate",
    "start": "nuxt-ts start"
  },
```

### add esLint for ts

```
$ yarn add -D @nuxtjs/eslint-config-typescript

yarn add v1.19.1
[1/4] 🔍  Resolving packages...
[2/4] 🚚  Fetching packages...
[3/4] 🔗  Linking dependencies...
warning "@nuxtjs/eslint-config-typescript > @nuxtjs/eslint-config@1.1.2" has unmet peer dependency "eslint@>=5.16.0".
warning "@nuxtjs/eslint-config-typescript > @nuxtjs/eslint-config > eslint-config-standard@12.0.0" has unmet peer dependency "eslint@>=5.0.0".
warning "@nuxtjs/eslint-config-typescript > @nuxtjs/eslint-config > eslint-plugin-import@2.18.2" has unmet peer dependency "eslint@2.x - 6.x".
warning "@nuxtjs/eslint-config-typescript > @nuxtjs/eslint-config > eslint-plugin-unicorn@9.1.1" has unmet peer dependency "eslint@>=5.0.0".
warning "@nuxtjs/eslint-config-typescript > @nuxtjs/eslint-config > eslint-plugin-jest@22.21.0" has unmet peer dependency "eslint@>=5".
warning "@nuxtjs/eslint-config-typescript > @typescript-eslint/parser@2.8.0" has unmet peer dependency "eslint@^5.0.0 || ^6.0.0".
warning "@nuxtjs/eslint-config-typescript > @typescript-eslint/eslint-plugin@2.8.0" has unmet peer dependency "eslint@^5.0.0 || ^6.0.0".
warning "@nuxtjs/eslint-config-typescript > @nuxtjs/eslint-config > eslint-plugin-standard@4.0.1" has unmet peer dependency "eslint@>=5.0.0".
warning "@nuxtjs/eslint-config-typescript > @nuxtjs/eslint-config > eslint-plugin-vue@5.2.3" has unmet peer dependency "eslint@^5.0.0".
warning "@nuxtjs/eslint-config-typescript > @nuxtjs/eslint-config > eslint-plugin-node@9.2.0" has unmet peer dependency "eslint@>=5.16.0".
warning "@nuxtjs/eslint-config-typescript > @typescript-eslint/eslint-plugin > tsutils@3.17.1" has unmet peer dependency "typescript@>=2.8.0 || >= 3.2.0-dev || >= 3.3.0-dev || >= 3.4.0-dev || >= 3.5.0-dev || >= 3.6.0-dev || >= 3.6.0-beta || >= 3.7.0-dev || >= 3.7.0-beta".
warning "@nuxtjs/eslint-config-typescript > @nuxtjs/eslint-config > eslint-plugin-vue > vue-eslint-parser@5.0.0" has unmet peer dependency "eslint@^5.0.0".
warning "@nuxtjs/eslint-config-typescript > @nuxtjs/eslint-config > eslint-plugin-node > eslint-plugin-es@1.4.1" has unmet peer dependency "eslint@>=4.19.1".
warning "@nuxtjs/eslint-config-typescript > @nuxtjs/eslint-config > eslint-plugin-jest > @typescript-eslint/experimental-utils@1.13.0" has unmet peer dependency "eslint@*".
warning "@nuxtjs/eslint-config-typescript > @typescript-eslint/parser > @typescript-eslint/experimental-utils@2.8.0" has unmet peer dependency "eslint@*".
[4/4] 🔨  Building fresh packages...
success Saved lockfile.
success Saved 49 new dependencies.
info Direct dependencies
└─ @nuxtjs/eslint-config-typescript@0.1.3
info All dependencies
├─ @nuxtjs/eslint-config-typescript@0.1.3
├─ @nuxtjs/eslint-config@1.1.2
├─ @types/eslint-visitor-keys@1.0.0
├─ @typescript-eslint/eslint-plugin@2.8.0
├─ @typescript-eslint/parser@2.8.0
├─ acorn-jsx@5.1.0
├─ array-includes@3.0.3
├─ clean-regexp@1.0.0
├─ contains-path@0.1.0
├─ doctrine@1.5.0
├─ eslint-ast-utils@1.1.0
├─ eslint-config-standard@12.0.0
├─ eslint-import-resolver-node@0.3.2
├─ eslint-module-utils@2.4.1
├─ eslint-plugin-es@1.4.1
├─ eslint-plugin-import@2.18.2
├─ eslint-plugin-jest@22.21.0
├─ eslint-plugin-node@9.2.0
├─ eslint-plugin-promise@4.2.1
├─ eslint-plugin-standard@4.0.1
├─ eslint-plugin-unicorn@9.1.1
├─ eslint-plugin-vue@5.2.3
├─ espree@4.1.0
├─ esquery@1.0.1
├─ find-up@2.1.0
├─ functional-red-black-tree@1.0.1
├─ hosted-git-info@2.8.5
├─ import-modules@1.1.0
├─ load-json-file@2.0.0
├─ locate-path@2.0.0
├─ lodash.camelcase@4.3.0
├─ lodash.defaultsdeep@4.6.1
├─ lodash.get@4.4.2
├─ lodash.snakecase@4.1.1
├─ lodash.topairs@4.3.0
├─ lodash.upperfirst@4.3.1
├─ lodash.zip@4.2.0
├─ normalize-package-data@2.5.0
├─ p-locate@2.0.0
├─ path-type@2.0.0
├─ read-pkg-up@2.0.0
├─ read-pkg@2.0.0
├─ regexp-tree@0.1.16
├─ reserved-words@0.1.2
├─ spdx-correct@3.1.0
├─ spdx-exceptions@2.2.0
├─ strip-bom@3.0.0
├─ validate-npm-package-license@3.0.4
└─ vue-eslint-parser@5.0.0
✨  Done in 4.02s.

```

### create .eslintrc.js

### change .eslintrc.js

```
# 下記を追加
  extends: [
    '@nuxtjs/eslint-config-typescript'
  ],
```
