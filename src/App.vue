<template>
  <div class="space-y-3">
    <h1 className="text-3xl font-bold underline">
      Late Night Woodworking
    </h1>

    <Carousel :image-urls="imageUrls" :auto-scroll="true" />
  
    <div>
      <a href="https://www.youtube.com/@LateNightWoodworking" target="_blank" class="btn btn-primary">
        Get 🪵
      </a>
    </div>
  </div>


</template>

<script setup lang="ts">
import { ref } from 'vue';
import Carousel from './components/Carousel.vue';

const imageUrls = ref([
  new URL('./assets/table1.webp', import.meta.url).href,
  new URL('./assets/table2.webp', import.meta.url).href,
  new URL('./assets/table3.webp', import.meta.url).href,
])
</script>
