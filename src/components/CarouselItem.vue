<template>
  <div :id="`item${index}`" class="carousel-item relative w-full">
    <img :src="model" class="w-full object-cover rounded-box" />
    <div class="absolute flex justify-between transform -translate-y-1/2 left-5 right-5 top-1/2">
      <a
        :href="`#item${index <= 0 ? length - 1 : index - 1}`"
        class="btn btn-sm btn-ghost btn-circle">❮</a> 
      <a
        :href="`#item${index >= length - 1 ? 0 : index + 1}`"
        class="btn btn-sm btn-ghost btn-circle"
        ref="nextBtn">❯</a>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const model = defineModel({ type: String });
const nextBtn = ref();

defineProps<{
  index: number,
  length: number,
}>();


defineExpose({
  clickNext,
});

function clickNext() {
  nextBtn.value.click();
}
</script>
