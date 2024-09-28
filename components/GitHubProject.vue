<script setup lang="ts">
import { ref } from 'vue'

const props = defineProps({
  org: {
    default: "",
  },
  repo: {
    default: "",
  },
  imgId: {
    default: "",
  },
})

const org = ref(props.org);
const repo = ref(props.repo);
const imgId = ref(props.imgId);
</script>

<template>
  <a :href="`https://github.com/${org}/${repo}`" class="w-full flex space-between p-4 rounded-lg shadow-lg !border-b-0">
    <div class="flex flex-col align-center gap-2 w-[90%]">
      <p class="!font-normal !text-2xl !leading-none">{{ org }}/</p>
      <p class="!text-2xl !m-0 !leading-none">{{ repo }}</p>
      <p class="!text-gray-400 !text-lg !font-normal !leading-none">github.com</p>
    </div>
    <div class="h-full flex self-center">
      <img class="!shadow-none" :src="`https://avatars.githubusercontent.com/u/${imgId}?s=150&v=4`" alt="" width="100" height="100">
    </div>
  </a>
</template>
