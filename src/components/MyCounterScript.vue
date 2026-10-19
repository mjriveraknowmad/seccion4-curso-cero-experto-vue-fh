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
  <button class="button-increment-multiply" @click="num++">Increment Num</button>
  <button class="button-increment-multiply" @click="multiple++">Multiply</button>
</template>

<style scoped>
.button-increment-multiply {
  @apply px-5 py-1 bg-blue-500 rounded mr-2 hover:bg-blue-700;
}
</style>
