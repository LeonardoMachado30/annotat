<template>
  <div
    class="flex flex-col items-center justify-center h-full content-center"
    v-if="list.length === 0"
  >
    <AddNoteDefault />
  </div>

  <div v-else class="flex flex-col justify-between w-full h-full">
    <div class="flex flex-col gap-2">
      <div
        v-for="item in list"
        v-bind:key="item.id"
        class="flex items-center rounded-md bg-white py-3 justify-around slide-top"
      >
        <input type="hidden" :value="item.id" />
        <div class="flex items-center gap-2">
          <PaperClipIcon class="h-5 w-5 text-gray-500" />
          <div class="flex flex-col">
            <p class="ellipse">{{ item.descripton }}</p>
            <p class="text-xs text-gray-500">{{ item.created_at }}</p>
          </div>
          <button>
            <TrashIcon class="h-6 w-6 text-red-400 opacity-70" />
          </button>
        </div>
      </div>
    </div>
    <ButtonPrimary to="/addnote" />
  </div>
</template>

<script setup lang="ts">
import { useEditor, EditorContent } from "@tiptap/vue-3";
import StarterKit from "@tiptap/starter-kit";
import Document from "@tiptap/extension-document";
import Paragraph from "@tiptap/extension-paragraph";
import Text from "@tiptap/extension-text";
import { PaperClipIcon, TrashIcon } from "@heroicons/vue/24/solid";
import AddNoteDefault from "~/components/AddNoteDefault.vue";
import ButtonPrimary from "~/components/Buttons/ButtonPrimary.vue";
import { ref } from "vue";
interface List {
  id: string;
  descripton: string;
  potential: number;
  category: Array<string>;
  reminder: string;
  created_at: string;
  updated_at: string;
}

const list = ref<Array<List>>([
  {
    id: "222-222-222-22",
    descripton: "Adicionar items da compra de carrinhos",
    potential: 0,
    category: ["asd"],
    reminder: "",
    created_at: "2023-20-1",
    updated_at: "2023-20-1",
  },
  {
    id: "222-222-222-22",
    descripton: "Adicionar items da compra de carrinhos",
    potential: 0,
    category: ["asd"],
    reminder: "",
    created_at: "2023-20-1",
    updated_at: "2023-20-1",
  },
]);

const editor = useEditor({
  content: "<p>I’m running Tiptap with Vue.js. 🎉</p>",
  autofocus: true,
  editable: true,
  extensions: [StarterKit, Document, Paragraph, Text],
});
</script>
