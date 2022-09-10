<script setup>
defineProps({
  error: Object
})
const handleError = () => clearError({ redirect: '/' })
</script>

<template>
  <div>
    <h2>Error</h2>
    <p>error : {{ error.message }}</p>
    <button @click="handleError">에러해결</button>
  </div>
</template>
<style scoped>

</style>