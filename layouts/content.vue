<script setup>
defineProps({
  subtitle: String | undefined,
});
</script>

<template>
  <div class="slidev-layout content">
    <div class="header">
      <div class="title" v-if="subtitle && $frontmatter.title">
        {{ $frontmatter.title }}
      </div>
      <div class="subtitle" v-if="subtitle || $frontmatter.title">
        {{ subtitle ?? $frontmatter.title }}
      </div>
    </div>
    <slot />
  </div>
</template>

<style>
.slidev-layout.content {
  @apply my-4;

  .header {
    @apply flex flex-col gap-1;

    .title {
      @apply text-lg font-bold;
    }

    .subtitle {
      @apply text-3xl font-bold;
    }
  }

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
}
</style>
