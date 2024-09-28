<template>
  <div>
    <div class="slidev-mockup-phone">
      <div class="camera"></div>
      <div class="display">
        <div class="artboard artboard-demo phone-1">
          <slot />
        </div>
      </div>
    </div>
  </div>
</template>

<!--
  This component style comes from DaisyUI, a Tailwind CSS component library.
  Learn more about DaisyUI at https://daisyui.com/
  DaisyUI GitHub repository: https://github.com/saadeghi/daisyui
  Licensed under the MIT License
-->

<style scoped>
  .slidev-mockup-phone {
    display: inline-block;
    border: 4px solid #444;
    border-radius: 50px;
    background-color: #000;
    padding: 10px;
    margin: 0 auto;
    overflow: hidden
  }

  .slidev-mockup-phone .camera {
    position: relative;
    top: 0;
    left: 0;
    background: #000;
    height: 25px;
    width: 150px;
    margin: 0 auto;
    border-bottom-left-radius: 17px;
    border-bottom-right-radius: 17px;
    z-index: 11;
  }

  .slidev-mockup-phone .camera:before {
    content: "";
    position: absolute;
    top: 35%;
    left: 50%;
    width: 50px;
    height: 4px;
    border-radius: 5px;
    background-color: #0c0b0e;
    transform: translate(-50%,-50%)
  }

  .slidev-mockup-phone .camera:after {
    content: "";
    position: absolute;
    top: 20%;
    left: 70%;
    width: 8px;
    height: 8px;
    border-radius: 5px;
    background-color: #0f0b25
  }
  .slidev-mockup-phone .display {
    overflow: hidden;
    border-radius: 40px;
    margin-top: -25px
  }

  .artboard-demo {
    border-radius: 1rem;
    background-color: oklch(0.924169 0.00108 197.138);
    box-shadow: 0 1px 3px #0000001a,0 1px 2px #0000000f;
  }

  .artboard-demo {
    display: flex;
    flex: none;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .artboard.phone-1 {
    width: 320px;
    height: 568px;
  }
</style>