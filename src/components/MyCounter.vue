<script setup lang="ts">
import { computed, ref } from 'vue';
// const props = withDefaults(
//   defineProps<{
//     value?: number;
//   }>(),
//   {
//     value: 0,
//   }
// );
// const props = defineProps<{
//     value: {
//         type: Number,
//         required: false,
//         default: 0
//     }
// }>();
const props = defineProps<{
    value: number;
}>();

const num = ref(+props.value);
const multiple = ref(1);
const count = computed(() => num.value  * multiple.value);

</script>

<template>
  <div>{{ num }} * {{ multiple }} = {{ count }}</div>
  <button @click="num++">Increment Num</button>
  <button @click="multiple++">Multiply</button>
</template>

<style scoped>
</style>
