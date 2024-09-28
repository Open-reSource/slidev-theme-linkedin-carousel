<template>
  <div class="slidev-layout cover">
    <div class="my-auto w-[600px] flex flex-col">
      <slot />
      <Author class="position-relative" />
    </div>
    <Swipe class="position-absolute end-[50px] top-[50%] translate-y-[-50%]" />
    <Save />
  </div>
</template>

<style>
  .slidev-layout.cover h2 {
    @apply opacity-75 text-xl;
  }
</style>
