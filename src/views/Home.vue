<template>
  <div class="w-full fixed">
    <Menu :transparent="true"></Menu>
  </div>

  <img :src="mainImg" class="min-h-[600px] object-cover" />

  <div class="flex">
    <div class="flex-1">
      <img :src="secondaryImg1" class="min-h-[600px] object-cover" />
    </div>
    <div class="flex-1">
      <img :src="secondaryImg2" class="min-h-[600px] object-cover" />
    </div>
  </div>
</template>

<script setup lang="ts">
import Menu from "../components/Menu.vue"

const mainImg = new URL('../assets/wall_small_16x9.jpg', import.meta.url).href

const secondaryImg1 = new URL('../assets/RH-6.jpg', import.meta.url).href
const secondaryImg2 = new URL('../assets/RH-8.jpg', import.meta.url).href
</script>
