<script setup lang="ts">
import { ref } from 'vue'

const props = defineProps({
  url: {
    default: "",
  },
})

const url = ref(props.url);
</script>

<template>
  <div class="slidev-mockup-browser bg-gray-200 border">
    <div class="slidev-mockup-browser-toolbar">
      <div class="input">{{ url }}</div>
    </div>
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
  .input {
    flex-shrink:1;
    -webkit-appearance: none;
    -moz-appearance: none;
    appearance: none;
    height: 3rem;
    padding-left: 1rem;
    padding-right: 1rem;
    font-size: 1rem;
    line-height: 2;
    line-height: 1.5rem;
    border-radius: .5rem;
    border-width: 1px;
    border-color: transparent;
  }

  .slidev-mockup-browser {
    position:relative;
    overflow:hidden;
    overflow-x:auto;
    border-radius: .5rem;
  }

  .slidev-mockup-browser pre[data-prefix]:before {
    content:attr(data-prefix);
    display:inline-block;
    text-align:right
  }

  .slidev-mockup-browser .slidev-mockup-browser-toolbar {
    margin-top: .75rem;
    margin-bottom: .75rem;
    display: inline-flex;
    width: 100%;
    align-items: center;
    padding-right: 1.4em;
  }

  .slidev-mockup-browser .slidev-mockup-browser-toolbar:before {
    content: "";
    margin-right: 4.8rem;
    display: inline-block;
    aspect-ratio: 1/1;
    height: .75rem;
    border-radius: 9999px;
    opacity: .3;
    box-shadow: 1.4em 0,2.8em 0,4.2em 0
  }

  .slidev-mockup-browser .slidev-mockup-browser-toolbar .input {
    position: relative;
    margin-left: auto;
    margin-right: auto;
    display: block;
    height: 1.75rem;
    width: 24rem;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
    background-color: oklch(0.961151 0 0);
    padding-left: 2rem;
  }
  .slidev-mockup-browser .slidev-mockup-browser-toolbar .input:before {
    content: "";
    position: absolute;
    left: .5rem;
    top: 50%;
    aspect-ratio: 1/1;
    height: .75rem;
    transform: matrix(1, 0, 0, 1, 0, -6);
    border-radius: 9999px;
    border-width: 2px;
    border-color: currentColor;
    opacity: .6;
  }
  .slidev-mockup-browser .slidev-mockup-browser-toolbar .input:after {
    content: "";
    position: absolute;
    left: 1.25rem;
    top: 50%;
    height: .5rem;
    transform: matrix(0.707107, -0.707107, 0.707107, 0.707107, 0, 2);
    border-radius: 9999px;
    border-width: 1px;
    border-color: currentColor;
    opacity: .6
  }
</style>