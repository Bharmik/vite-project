<template>
  <h1>{{titleText}}</h1>
  <LifeDemo />
</template>

<script setup>
import {ref} from 'vue'
import LifeDemo from '../components/LifeDemo.vue'

const titleText = ref('index')
</script>

<style lang="less" scoped>

</style>