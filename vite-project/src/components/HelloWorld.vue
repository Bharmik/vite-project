<script setup>
import { ref } from 'vue'

defineProps({
  msg: String
})

const count = ref(0)
</script>

<template>
  <h1>{{ msg }}</h1>

  <p>
    推荐的 IDE 设置：
    <a href="https://code.visualstudio.com/" target="_blank">VSCode</a>
    +
    <a href="https://github.com/johnsoncodehk/volar" target="_blank">Volar</a>
  </p>

  <p>
    <a href="https://vitejs.dev/guide/features.html" target="_blank">
      Vite 文档
    </a>
    |
    <a href="https://v3.vuejs.org/" target="_blank">Vue 3 文档</a>
  </p>

  <button type="button" @click="count++">count is: {{ count }}</button>
  <p class="text">
    Edit
    <code class="code">components/HelloWorld.vue</code> to test hot module replacement.
  </p>
</template>

<style lang="less" scoped>
a {
  color: #42b983;
}
.text{
  color: red;
  .code{
    color: blue;
  }
}
</style>
