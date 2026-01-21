<script setup>
defineProps(["subtitle"]);
</script>

<template>
  <div class="flex flex-col gap-1">
    <div class="text-lg font-bold">{{ subtitle }}</div>
    <div class="text-3xl font-bold">
      <slot />
    </div>
  </div>
</template>
