<template>
  <div
    class="font-bold text-2xl text-gray-600 w-full text-start mt-2 mb-6 slide-top"
  >
    {{ title }}
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";
const route = useRoute();
const title = ref<string>("");
console.log(route);

if (route.path.includes("/addnote")) {
  title.value = "Adicionar";
} else {
  title.value = "Anotações";
}
</script>
