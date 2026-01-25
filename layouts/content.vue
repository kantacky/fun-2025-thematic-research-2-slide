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

  h1,
  h2,
  h3,
  h4,
  h5,
  h6 {
    @apply m-0;
    @apply font-bold mt-2;
  }

  h1 {
    @apply text-xl;
  }
  h2 {
    @apply text-lg;
  }
  h3,
  h4,
  h5,
  h6 {
    @apply text-base;
  }

  .page-number {
    @apply absolute top-10 right-14 text-2xl font-bold;
  }

  .content {
    @apply flex flex-col gap-2 text-lg;
  }

  .header {
    @apply flex flex-col border-b border-gray-400;

    .title {
      @apply ml-0.5;
      @apply text-base font-bold;
    }

    .subtitle {
      @apply text-2xl font-bold;
    }
  }

  ul {
    @apply list-disc list-inside;
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
