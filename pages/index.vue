<script setup lang="ts">
/**
 * app.config.ts
 * export default defineAppConfig({})
 */
import {useAppConfig,showError } from '#app'
import Uncle from "~/components/uncle.vue";
const route = useRoute()
if ('setup' in route.query) {
  throw new Error('error in setup')
}
if ('mounted' in route.query) {
  onMounted(() => {
    throw new Error('error in mounted')
  })
}
function triggerError () {
  throw new Error('manually triggered error')
}
const appConfig = useAppConfig();



</script>
<script lang="ts">
import {definePageMeta} from "#imports";

// routing 시 layout 설정
definePageMeta({
  title: 'Home',
})
</script>
<template>
  <div>
    <h1>{{appConfig.title}}</h1>
    <p>{{appConfig.description}}</p>
    <NuxtLink to="/about">
      about 페이지로
    </NuxtLink>
    <NuxtLink to="/other">
      other 페이지로
    </NuxtLink>
    <NuxtLink to="/?middleware" class="n-link-base">
          Middleware
        </NuxtLink>
     <button class="n-link-base" @click="showError">
          Trigger fatal error
        </button>
        <button class="n-link-base" @click="triggerError">
          Trigger non-fatal error
        </button>
    <figure>
      <img src="/img/images.jpg" alt="위 베어 베어스 귀엽다" />
    </figure>
    <p>public 폴더에 로컬 미디어 데이터를 넣고 사용 가능</p>
    <Uncle />
    <ParentChild />
    <Wrapper>
      <p>이건 app에서 씀</p>
    </Wrapper>
  </div>
</template>
