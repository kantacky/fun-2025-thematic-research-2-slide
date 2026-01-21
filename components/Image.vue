<script setup>
defineProps(["image", "caption", "index", "class"]);
</script>

<template>
  <div :class="class">
    <img
      class="w-full outline outline-1 outline-gray-300 my-2 p-2"
      :src="`${image}`"
      :alt="caption"
    />
  </div>
  <div v-if="index" class="text-center text-xs">
    {{ caption }} <Cite :index="index" />
  </div>
  <div v-else class="text-center text-xs">
    {{ caption }}
  </div>
</template>
