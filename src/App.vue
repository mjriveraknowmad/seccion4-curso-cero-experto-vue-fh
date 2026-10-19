<script setup lang="ts">
import MyCounter from './components/MyCounter.vue';
import MyCounterScript from './components/MyCounterScript.vue';
import MyCounterScriptExternal from './components/my-counter-script/MyCounterScriptExternal.vue';
</script>

<template>
  <MyCounter :value="1" />
  <MyCounterScript :value="1" />
  <MyCounterScriptExternal :value="1" />
</template>

<style scoped>
</style>
