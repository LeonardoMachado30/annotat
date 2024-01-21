<template>
  <main
    class="max-auto flex flex-col justify-start items-center top-20 p-4 h-screen"
  >
    <Header />
    <NuxtPage />
  </main>
</template>

<script setup lang="ts">
import "public/css/global.css";
useHead({ title: "annotat" });
</script>
