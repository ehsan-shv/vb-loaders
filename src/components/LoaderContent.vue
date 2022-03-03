<template>
  <div class="vb-loaderContent" :class="{ blur }">
    <slot />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'LoaderContent',
  props: {
    blur: {
      type: Boolean,
      default: false,
    },
  },
});
</script>

<style lang="scss">
:root {
  --vb-loader-content-background-color: #212121;
  --vb-loader-content-opacity: 0.6;
  --vb-loader-content-z-index: 999;
  --vb-loader-content-glass-blur: 20px;
  --vb-loader-content-glass-background: rgba(255, 255, 255, 0.25);
}
.vb-loaderContent {
  position: relative;
  z-index: var(--vb-loader-content-z-index);

  &.blur {
    &::after {
      background: var(--vb-loader-content-glass-background);
      backdrop-filter: blur(var(--vb-loader-content-glass-blur));
      -webkit-backdrop-filter: blur(var(--vb-loader-content-glass-blur));
      opacity: 1;
    }
  }

  &::after {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: var(--vb-loader-content-background-color);
    opacity: var(--vb-loader-content-opacity);
  }
}
</style>
