<template>
  <div class="vb-loaderContent" :class="{ blur, fullScreen, disable: !disable }">
    <slot />
    <LoaderFacebook v-if="innerLoader === 'LoaderFacebook' && disable" />
    <LoaderDualRing v-if="innerLoader === 'LoaderDualRing' && disable" />
    <LoaderCircle v-if="innerLoader === 'LoaderCircle' && disable" />
    <LoaderRoller v-if="innerLoader === 'LoaderRoller' && disable" />
    <LoaderRing v-if="innerLoader === 'LoaderRing' && disable" />
    <LoaderHeart v-if="innerLoader === 'LoaderHeart' && disable" />
    <LoaderGrid v-if="innerLoader === 'LoaderGrid' && disable" />
    <LoaderEllipsis v-if="innerLoader === 'LoaderEllipsis' && disable" />
    <LoaderDefault v-if="innerLoader === 'LoaderDefault' && disable" />
    <LoaderSpinner v-if="innerLoader === 'LoaderSpinner' && disable" />
    <LoaderRipple v-if="innerLoader === 'LoaderRipple' && disable" />
    <LoaderHourglass v-if="innerLoader === 'LoaderHourglass' && disable" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import LoaderCircle from './LoaderCircle.vue';
import LoaderFacebook from './LoaderFacebook.vue';
import LoaderDualRing from './LoaderDualRing.vue';
import LoaderRoller from './LoaderRoller.vue';
import LoaderRing from './LoaderRing.vue';
import LoaderHeart from './LoaderHeart.vue';
import LoaderGrid from './LoaderGrid.vue';
import LoaderEllipsis from './LoaderEllipsis.vue';
import LoaderDefault from './LoaderDefault.vue';
import LoaderSpinner from './LoaderSpinner.vue';
import LoaderRipple from './LoaderRipple.vue';
import LoaderHourglass from './LoaderHourglass.vue';

export default defineComponent({
  name: 'LoaderContent',
  components: {
    LoaderFacebook,
    LoaderDualRing,
    LoaderCircle,
    LoaderRoller,
    LoaderRing,
    LoaderHeart,
    LoaderGrid,
    LoaderEllipsis,
    LoaderDefault,
    LoaderSpinner,
    LoaderRipple,
    LoaderHourglass,
  },
  props: {
    blur: {
      type: Boolean,
      default: false,
    },
    disable: {
      type: Boolean,
      default: false,
    },
    innerLoader: {
      type: String,
      default: '',
    },
    fullScreen: {
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
  --vb-loader-content-inner-loader-z-index: 1000;
  --vb-loader-content-glass-blur: 15px;
  --vb-loader-content-glass-background: rgba(255, 255, 255, 0.25);
}
.vb-loaderContent {
  position: relative;
  z-index: var(--vb-loader-content-z-index);

  &.disable {
    &::after,
    .vb-loader {
      display: none;
    }
  }

  &.fullScreen {
    &::after,
    .vb-loader {
      position: fixed;
    }
  }

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

  .vb-loader {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: var(--vb-loader-content-inner-loader-z-index);
  }
}
</style>
