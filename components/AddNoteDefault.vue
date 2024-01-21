<template>
  <span class="flex flex-col items-center">
    <PaperClipIcon class="h-20 w-20 text-gray-500 mb-8" />

    <h1 class="text-[#1b96f3] font-bold text-3xl">Anotações</h1>
    <p class="text-gray-400">by Speedio</p>
  </span>

  <ButtonPrimary />
</template>

<script setup lang="ts">
import { PaperClipIcon } from "@heroicons/vue/24/solid";
import ButtonPrimary from "@@/components/Buttons/ButtonPrimary.vue";

</script>