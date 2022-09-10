# Nuxt 3 실습용 프로젝트

해당 프로젝트는 Nuxt 3를 학습하기 위하여 [nuxt 3 documentation](https://v3.nuxtjs.org)을 보면서 실습한 연습용 프로젝트입니다.
Nuxt.js 에서 제공하는 Nuxt 3 Minimal Starter 를 이용하여 세팅되었습니다.

## Setup

yarn 안씀.

```bash
# npm
npm install
```

## Development Server

Start the development server on http://localhost:3000

```bash
npm run dev
```

## Production

Build the application for production:

```bash
npm run build
```

Locally preview production build:

```bash
npm run preview
```

Checkout the [deployment documentation](https://v3.nuxtjs.org/guide/deploy/presets) for more information.

## Head 관리

즉시 사용할 수 있는 Nuxt는 `charset` 및 `viewport` 메타 태그에 대한 좋은 기본값을 제공하지만 필요한 경우 이러한 값을 재정의할 수 있으며 여러 가지 방법으로 사이트에 대한 다른 메타 태그를 사용자 지정할 수 있습니다.

> [`<head>` 태그 document](https://v3.nuxtjs.org/api/configuration/nuxt.config#head)

설정 함수 내에서 `useHead`를 메타데이터 태그(`title`, `titleTemplate`, `base`, `script`, `noscript`, `style`, `meta` 및 `link`, `htmlAttrs` 및 `bodyAttrs`)에 해당하는 키로 호출할 수 있습니다. 또한 해당 메타 태그를 설정하는 `charset` 및 `viewport`라는 두 가지 단축 속성이 있습니다. 또는 사후 대응 메타데이터에 대해 개체를 반환하는 함수를 전달할 수 있습니다.

```vue
<script setup>
useHead({
  title: 'My App',
  // or, instead:
  // titleTemplate: (title) => `My App - ${title}`,
  viewport: 'width=device-width, initial-scale=1, maximum-scale=1',
  charset: 'utf-8',
  meta: [
    { name: 'description', content: 'My amazing site.' }
  ],
  bodyAttrs: {
    class: 'test'
  }
})
</script>
```