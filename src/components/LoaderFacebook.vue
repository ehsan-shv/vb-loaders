<template>
  <div class="vb-loader lds-facebook">
    <div />
    <div />
    <div />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'LoaderFacebook',
});
</script>

<style lang="scss">
:root {
  --vb-loader-facebook-background-color: #ffffff;
}

.vb-loader.lds-facebook {
  display: inline-block;
  position: relative;
  width: 80px;
  height: 80px;
}
.vb-loader.lds-facebook div {
  display: inline-block;
  position: absolute;
  left: 8px;
  width: 16px;
  background: var(--vb-loader-facebook-background-color);
  animation: lds-facebook 1.2s cubic-bezier(0, 0.5, 0.5, 1) infinite;
}
.vb-loader.lds-facebook div:nth-child(1) {
  left: 8px;
  animation-delay: -0.24s;
}
.vb-loader.lds-facebook div:nth-child(2) {
  left: 32px;
  animation-delay: -0.12s;
}
.vb-loader.lds-facebook div:nth-child(3) {
  left: 56px;
  animation-delay: 0;
}
@keyframes lds-facebook {
  0% {
    top: 8px;
    height: 64px;
  }
  50%,
  100% {
    top: 24px;
    height: 32px;
  }
}
</style>
