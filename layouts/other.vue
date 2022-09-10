<template>
<div>
  <h1>other layout 입니다.</h1>
  <hr>
  <slot />
</div>
</template>
<script setup>
  useHead({
    title:"Other",
    titleTemplate: (titleChunk) => {
      return titleChunk ? `Nuxt app - ${titleChunk}` : '??';
    }
  })
</script>
<script>
export default {
  name: "other"
}
</script>

<style scoped>
h1 {
  color: red;
}
</style>