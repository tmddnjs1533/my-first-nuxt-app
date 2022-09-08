<script setup>
/**
 * app.config.ts
 */
const config = useAppConfig();
</script>
<template>
  <div>
    <h1>{{config.title}}</h1>
    <p>{{config.description}}</p>
  </div>
</template>

