<template>
  <div class="carousel carousel-center p-4 space-x-4 bg-neutral rounded-box max-w-[800px] max-h-[400px]">
    <template v-for="(imageUrl, index) in props.imageUrls" :key="imageUrl">
      <div :id="`item${index}`" class="carousel-item relative w-full">
        <img  :src="imageUrl" class="w-full object-cover rounded-box" />
        <div class="absolute flex justify-between transform -translate-y-1/2 left-5 right-5 top-1/2">
          <a :href="getPrevId(index)" class="btn btn-sm btn-ghost btn-circle">❮</a> 
          <a :href="getNextId(index)" class="btn btn-sm btn-ghost btn-circle">❯</a>
        </div>
      </div>
    </template>
  </div>
</template>

<script setup lang="ts">
const props = defineProps<{
    imageUrls: string[]
}>();

function getPrevId(index: number): string {
  let prevIndex = index - 1;
  if (prevIndex < 0) {
    prevIndex = props.imageUrls.length - 1;
  }
  return `#item${prevIndex}`;
}

function getNextId(index: number): string {
  let nextIndex = index + 1;
  if (nextIndex >= props.imageUrls.length) {
    nextIndex = 0;
  }
  return `#item${nextIndex}`;
}

</script>
