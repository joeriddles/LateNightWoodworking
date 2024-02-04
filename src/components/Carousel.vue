<template>
  <div class="carousel carousel-center p-4 space-x-4 bg-base-300 rounded-box max-w-[800px] max-h-[400px]">
    <CarouselItem v-for="(imageUrl, index) in props.imageUrls" :key="imageUrl" :model-value="imageUrl" :index="index"
      :length="props.imageUrls.length" ref="items" />
  </div>
</template>

<script setup lang="ts">
import { Ref, onMounted, onUnmounted, ref } from 'vue';
import CarouselItem from './CarouselItem.vue';

let intervalID: number | null;
const items: Ref<any[]> = ref([]);
// const index: Ref<number> = ref(0);

const props = defineProps<{
  imageUrls: string[],
  autoScroll: boolean,
}>();

onMounted(() => {
  if (props.autoScroll) {
    // intervalID = setInterval(() => {
    //   let newIndex = index.value + 1;
    //   if (newIndex === props.imageUrls.length) {
    //     newIndex = 0;
    //   }
    //   items.value[newIndex].clickNext();
    //   index.value = newIndex;
    // }, 3_000);
  }
});

onUnmounted(() => {
  if (intervalID) {
    clearInterval(intervalID);
  }
})
</script>
