<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HeaderComponent from '@/components/HeaderComponent.vue'
</script>

<template>
  <div class="flex flex-col h-screen">
  <HeaderComponent/>
  <RouterView />
  </div>
</template>

<style>
</style>