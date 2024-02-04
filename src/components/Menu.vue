<template>
  <div class="navbar bg-base-100">
    <div class="flex-1">
      <router-link to="/" class="btn btn-ghost text-xl">Late Night Woodworking</router-link>
    </div>
    <div class="flex-none">
      <ul class="menu menu-horizontal px-1">
        <li><router-link to="/">Home</router-link></li>
        <li><router-link to="/gallery">Gallery</router-link></li>
        <li><router-link to="/about">About</router-link></li>
      </ul>
    </div>
  </div>
</template>
