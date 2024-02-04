<template>
  <div class="text-center w-full flex justify-center" :class="{ 'bg-red-700': !$props.transparent }">
    <div class="navbar justify-center bg-transparent px-[100px] pt-4">
      <div class="flex-1">
        <router-link to="/">
          <img :src="img" />
        </router-link>
      </div>
      <div class="flex-none">
        <ul class="menu menu-horizontal px-1 text-white uppercase">
          <li><router-link to="/">Home</router-link></li>
          <li><router-link to="/gallery">Gallery</router-link></li>
          <li><router-link to="/about">About</router-link></li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import img from "../assets/logo_small.png"

defineProps<{
  transparent: boolean,
}>();

</script>
