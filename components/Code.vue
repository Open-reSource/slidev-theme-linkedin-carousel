<template>
  <div class="slidev-mockup-code">
    <slot />
  </div>
</template>

<!--
  This component style comes from DaisyUI, a Tailwind CSS component library.
  Learn more about DaisyUI at https://daisyui.com/
  DaisyUI GitHub repository: https://github.com/saadeghi/daisyui
  Licensed under the MIT License
-->

<style>
  .slidev-mockup-code {
    position:relative;
    overflow:hidden;
    overflow-x:auto;
    min-width:18rem;
    border-radius: 1rem;
    --tw-bg-opacity: 1;
    background-color: oklch(0.321785 0.02476 255.702);
    padding-top:1.25rem;
    padding-bottom:1.25rem;
    --tw-text-opacity: 1;
    color: oklch(0.894994 0.011585 252.096);
    direction:ltr
  }

  .slidev-mockup-code pre[data-prefix]:before {
    content: attr(data-prefix);
    display: inline-block;
    text-align: right;
    width: 2rem;
    opacity: .5
  }

  .slidev-mockup-code:before {
    content: "";
    margin-bottom: 1rem;
    display: block;
    height: .75rem;
    width: .75rem;
    border-radius: 9999px;
    opacity: .3;
    box-shadow: 1.4em 0,2.8em 0,4.2em 0
  }

  .slidev-mockup-code pre {
    padding-right: 1.25rem
  }

  .slidev-mockup-code pre:before {
    content: "";
    margin-right: 2ch
  }
</style>