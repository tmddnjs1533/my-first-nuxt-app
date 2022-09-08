<script setup>
/**
 * app.config.ts
 */
const config = useAppConfig();

</script>
<script>
definePageMeta({
  layout: 'default'
})
</script>
<template>
  <div>
    <h1>{{config.title}}</h1>
    <p>{{config.description}}</p>
    <NuxtLink to="/other">
      other 페이지로
    </NuxtLink>
  </div>
</template>
