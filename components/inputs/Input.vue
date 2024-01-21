<template>
  <span :html-for="title" class="text-gray-500">{{ title }}</span>
  <div class="relative">
    <input
      class="px-6 h-16 placeholder:text-gray-500 w-full rounded-full focus:border-[#2E76BE] focus:!border-none focus:shadow-md focus:outline-none focus:transition focus:duration-800"
      :placeholder="placeholder"
      :type="type"
    />
    <div class="absolute right-5 top-5">
      <slot></slot>
    </div>
  </div>
</template>

<script setup lang="ts">
const { title, placeholder } = defineProps({
  title: { type: String },
  placeholder: { type: String },
  type: { type: String },
});
</script>
