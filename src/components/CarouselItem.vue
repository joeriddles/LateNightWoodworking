<template>
  <div :id="`item${index}`" class="carousel-item relative w-full">
    <img :src="model" class="w-full object-cover rounded-box" />
    <div class="absolute flex justify-between transform -translate-y-1/2 left-5 right-5 top-1/2">
      <a :href="prevHref" class="btn btn-sm btn-ghost btn-circle">❮</a> 
      <a :href="nextHref" class="btn btn-sm btn-ghost btn-circle" ref="nextBtn">❯</a>
    </div>
  </div>
</template>

<script setup lang="ts">
import { onMounted, ref } from 'vue';

const model = defineModel({ type: String });
const nextBtn = ref();
const prevHref = ref();
const nextHref = ref();

const props = defineProps<{
  index: number,
  length: number,
}>();

defineExpose({
  clickNext,
});

onMounted(() => {
  prevHref.value = `#item${props.index <= 0 ? props.length - 1 : props.index - 1}`;
  nextHref.value = `#item${props.index >= props.length - 1 ? 0 : props.index + 1}`;
})

function clickNext() {
  nextBtn.value.click();
}
</script>
