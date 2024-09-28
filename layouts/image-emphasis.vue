<template>
  <div class="slidev-layout image-emphasis">
    <div class="slidev-layout-image-emphasis-container my-auto w-full flex flex-col items-center">
      <slot />
    </div>
    <Author class="position-absolute bottom-[50px]" />
    <Save />
  </div>
</template>

<style>
  .slidev-layout-image-emphasis-container p {
    @apply text-5xl my-1 font-bold;
  }
</style>
