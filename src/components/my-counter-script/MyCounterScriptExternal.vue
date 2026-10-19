<script lang="ts" src="./MyCounterScriptExternal.ts"></script>

<template>
  <div>{{ num }} * {{ multiple }} = {{ count }}</div>
  <button @click="num++">Increment Num</button>
  <button @click="multiple++">Multiply</button>
</template>

<style scoped>
</style>
