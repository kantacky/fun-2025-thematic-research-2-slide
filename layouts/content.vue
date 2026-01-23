<script setup>
defineProps({
  subtitle: String | undefined,
});
</script>

<template>
  <div class="slidev-layout">
    <div class="page-number">{{ $page }}</div>
    <div class="content">
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
  </div>
</template>

<style>
.slidev-layout {
  @apply relative;

  .page-number {
    @apply absolute top-8 right-12 text-2xl font-bold;
  }

  .content {
    @apply flex flex-col gap-2 text-xl;
  }

  .header {
    @apply flex flex-col;

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

  table {
    @apply my-8;
    th,
    td {
      @apply border-b border-gray-400;
    }
  }
}
</style>
