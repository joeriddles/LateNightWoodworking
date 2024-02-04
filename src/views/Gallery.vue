<template>
  <Menu></Menu>

  <div class="w-full text-center space-y-3">
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
import Carousel from '../components/Carousel.vue';
import Menu from "../components/Menu.vue"

const imageUrls = ref([
  new URL('../assets/RH-4.jpg', import.meta.url).href,
  new URL('../assets/RH-6.jpg', import.meta.url).href,
  new URL('../assets/RH-8.jpg', import.meta.url).href,
  new URL('../assets/RH-10.jpg', import.meta.url).href,
])
</script>
