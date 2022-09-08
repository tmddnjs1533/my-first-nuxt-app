<template>
<div>
  <h1>other layout 입니다.</h1>
  <hr>
  <slot />
</div>
</template>

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