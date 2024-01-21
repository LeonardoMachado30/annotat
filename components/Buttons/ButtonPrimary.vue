<template>
  <NuxtLink
    :to="to"
    class="flex items-center bg-[#1b96f3] text-white px-5 py-3 rounded-full gap-2 mt-8 w-full justify-center"
  >
    <PlusIcon class="h-6 w-6 text-white" />
    <p>{{ title }}</p>
  </NuxtLink>
</template>

<script setup lang="ts">
import { PlusIcon } from "@heroicons/vue/24/solid";
const { to, title } = defineProps({
  to: { type: String, default: "/" },
  title: { type: String, default: "Criar anotação" },
});
</script>
