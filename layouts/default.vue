<template>
  <div class="slidev-layout default">
    <div class="slidev-layout-default-container my-auto w-full flex flex-col">
      <slot />
    </div>
    <Author class="position-absolute bottom-[50px]" />
    <Save />
  </div>
</template>

<style>
  .slidev-layout-default-container p {
    @apply text-5xl my-1 font-bold;
  }
</style>
