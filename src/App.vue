<template>
  <div class="space-y-3">
    <h1 className="text-3xl font-bold underline">
      Late Night Woodworking
    </h1>
  
    <div class="carousel carousel-center p-4 space-x-4 bg-neutral rounded-box max-w-[800px] max-h-[400px]">
      <div id="item1" class="carousel-item relative w-full">
        <img :src="table1Url" class="w-full object-cover rounded-box" />
        <div class="absolute flex justify-between transform -translate-y-1/2 left-5 right-5 top-1/2">
          <a href="#item3" class="btn btn-sm btn-ghost btn-circle">❮</a> 
          <a href="#item2" class="btn btn-sm btn-ghost btn-circle">❯</a>
        </div>
      </div>
      <div id="item2" class="carousel-item relative w-full">
        <img :src="table2Url" class="w-full object-cover rounded-box" />
        <div class="absolute flex justify-between transform -translate-y-1/2 left-5 right-5 top-1/2">
          <a href="#item1" class="btn btn-sm btn-ghost btn-circle">❮</a> 
          <a href="#item3" class="btn btn-sm btn-ghost btn-circle">❯</a>
        </div>
      </div>
      <div id="item3" class="carousel-item relative w-full">
        <img :src="table3Url" class="w-full object-cover rounded-box" />
        <div class="absolute flex justify-between transform -translate-y-1/2 left-5 right-5 top-1/2">
          <a href="#item2" class="btn btn-sm btn-ghost btn-circle">❮</a> 
          <a href="#item1" class="btn btn-sm btn-ghost btn-circle">❯</a>
        </div>
      </div>
    </div>
  
    <div>
      <a href="https://www.youtube.com/@LateNightWoodworking" target="_blank" class="btn btn-primary">
        Get 🪵
      </a>
    </div>
  </div>


</template>

<script setup lang="ts">
import { ref } from 'vue';

const table1Url = ref(new URL('./assets/table1.webp', import.meta.url).href)
const table2Url = ref(new URL('./assets/table2.webp', import.meta.url).href)
const table3Url = ref(new URL('./assets/table3.webp', import.meta.url).href)
</script>

<style scoped>
</style>
