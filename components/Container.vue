<template>
  <div class="my-4">
    <slot />
  </div>
</template>

<style>
.split {
  @apply flex flex-row gap-4;
  > div {
    @apply flex-1;
  }
}

li {
  @apply my-1;
}

table {
  @apply my-8;
  th,
  td {
    @apply border-b border-gray-400;
  }
}
</style>
