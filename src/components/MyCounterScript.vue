<script lang="ts">
import { computed, defineComponent, ref } from 'vue';
export default defineComponent({
  props: {
    value: {
      type: Number,
      required: true
    }
  },
  setup(props) {
    const num = ref(+props.value);
    const multiple = ref(1);
    const count = computed(() => num.value * multiple.value);
    return { num, multiple, count };
  }
});
</script>

<template>
  <div>{{ num }} * {{ multiple }} = {{ count }}</div>
  <button @click="num++">Increment Num</button>
  <button @click="multiple++">Multiply</button>
</template>

<style scoped>
</style>
