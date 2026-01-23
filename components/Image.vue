<script setup>
defineProps(["image", "caption", "index", "class"]);
</script>

<template>
  <div :class="class">
    <img
      class="w-full h-full object-contain outline outline-1 outline-gray-300 my-1"
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
