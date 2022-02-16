<template>
  <div>
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld v-model="value" />
  </div>
</template>

<script lang="ts" setup>
import HelloWorld from './components/HelloWorld.vue'
import { ref } from '@vue/composition-api'

const value = ref('1')
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>