<template>
  <form class="flex flex-col justify-between gap-2 w-full h-full slide-top">
    <div class="flex flex-col gap-1">
      <Input type="text" />
      <Input type="text" title="Potencial de negocio" placeholder="0" />

      <Input
        type="text"
        title="Categorização"
        placeholder="importante, não importante, bom, ruim ..."
      >
        <CalendarDaysIcon class="h-6 w-6 text-gray-500" />
      </Input>

      <Input type="date" title="Lembrete" placeholder="20 de agosto 2023">
        <CalendarDaysIcon  class="h-6 w-6 text-gray-500" />
      </Input>
    </div>
    <ButtonPrimary title="Salvar" />
  </form>
</template>

<script setup lang="ts">
import Input from "@@/components/inputs/Input.vue";
import ButtonPrimary from "@@/components/Buttons/ButtonPrimary.vue";
import { CalendarDaysIcon } from "@heroicons/vue/24/outline";
</script>
