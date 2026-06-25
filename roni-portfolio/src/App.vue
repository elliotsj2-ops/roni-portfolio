<script setup lang="ts">
import { RouterView } from 'vue-router';
</script>

<template>
  <nav class="flex flex-row items-center justify-between text-black text-base p-4 gap-4 bg-white/30 fixed top-0 left-0 w-full h-16 z-50 backdrop-blur-md">
    <div class="font-montserrat flex-1 flex flex-row gap-8 text-sm md:text-lg">
      <router-link to="/">Home</router-link>
      <router-link to="/about">About Me</router-link>
    </div>
    <div class="font-playfair text-lg font-bold flex-none text-gray-800">
      <router-link to="/">Regenerative Teaching Consulting</router-link>
    </div>
    <div class="flex-1 flex"></div>
  </nav>
  <RouterView />
</template>
