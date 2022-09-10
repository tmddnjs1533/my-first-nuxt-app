<script setup lang="ts">

</script>

<script lang="ts">
export default {
  name: "wrapper"
}
</script>

<template>
<div>
  <h2>wrapper</h2>
  <p>이 아래로 슬롯</p>
  <Slot />
</div>
</template>

<style scoped>

</style>