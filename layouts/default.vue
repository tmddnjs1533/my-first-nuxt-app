<template>
<div>
  <h1>default layout 입니다.</h1>
  <hr>
  <slot />
</div>
</template>

<script lang="ts">
export default {
  name: "default"
}
</script>

<script setup lang="ts">
useHead({
  // or, instead:
  titleTemplate: (title) => `Nuxt app - ${title}`,
  viewport: 'width=device-width, initial-scale=1, maximum-scale=1',
  charset: 'utf-8',
  meta: [
    { name: 'description', content: '첫 nuxt app 입니다.' }
  ],
  bodyAttrs: {
    class: 'root'
  }
})

</script>

<style scoped>

</style>