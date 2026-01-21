<script setup>
defineProps(["index", "caption"]);
</script>

<template>
  <div class="flex items-start gap-2 text-xs opacity-75">
    <div>[{{ index }}]</div>
    <div>
      {{ caption }}
    </div>
  </div>
</template>
