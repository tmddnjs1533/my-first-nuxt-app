<script setup lang="ts">
/**
 * app.config.ts
 */
const appConfig = useAppConfig();

</script>
<script>
definePageMeta({
  layout: 'default'
})
</script>
<template>
  <div>
    <h1>{{appConfig.title}}</h1>
    <p>{{appConfig.description}}</p>
    <NuxtLink to="/other">
      other 페이지로
    </NuxtLink>
    <figure>
      <img src="/img/images.jpg" alt="위 베어 베어스 귀엽다" />
    </figure>
  </div>
</template>
