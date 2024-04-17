<template>
  <div class="p-10 bg-gray-500 h-full space-y-10">
    <p>Component: demoFolder/demo</p>
    <p>composable: {{ demoComposable }}</p>
    <p>API: {{ demoApi }}</p>
    <demoFolder-BtnBlue></demoFolder-BtnBlue>
  </div>
</template>

<script setup>
import { useDemo } from "@/composables/demoFolder/demo";

const demoComposable = useDemo();
const demoApi = await $fetch("/api/auth/demo");
</script>
