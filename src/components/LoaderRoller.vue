<template>
  <div class="vb-loader lds-roller">
    <div />
    <div />
    <div />
    <div />
    <div />
    <div />
    <div />
    <div />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'LoaderRoller',
});
</script>

<style lang="scss">
:root {
  --vb-loader-roller-background-color: #ffffff;
}
.vb-loader.lds-roller {
  display: inline-block;
  position: relative;
  width: 80px;
  height: 80px;
}
.vb-loader.lds-roller div {
  animation: lds-roller 1.2s cubic-bezier(0.5, 0, 0.5, 1) infinite;
  transform-origin: 40px 40px;
}
.vb-loader.lds-roller div:after {
  content: ' ';
  display: block;
  position: absolute;
  width: 7px;
  height: 7px;
  border-radius: 50%;
  background: var(--vb-loader-roller-background-color);
  margin: -4px 0 0 -4px;
}
.vb-loader.lds-roller div:nth-child(1) {
  animation-delay: -0.036s;
}
.vb-loader.lds-roller div:nth-child(1):after {
  top: 63px;
  left: 63px;
}
.vb-loader.lds-roller div:nth-child(2) {
  animation-delay: -0.072s;
}
.vb-loader.lds-roller div:nth-child(2):after {
  top: 68px;
  left: 56px;
}
.vb-loader.lds-roller div:nth-child(3) {
  animation-delay: -0.108s;
}
.vb-loader.lds-roller div:nth-child(3):after {
  top: 71px;
  left: 48px;
}
.vb-loader.lds-roller div:nth-child(4) {
  animation-delay: -0.144s;
}
.vb-loader.lds-roller div:nth-child(4):after {
  top: 72px;
  left: 40px;
}
.vb-loader.lds-roller div:nth-child(5) {
  animation-delay: -0.18s;
}
.vb-loader.lds-roller div:nth-child(5):after {
  top: 71px;
  left: 32px;
}
.vb-loader.lds-roller div:nth-child(6) {
  animation-delay: -0.216s;
}
.vb-loader.lds-roller div:nth-child(6):after {
  top: 68px;
  left: 24px;
}
.vb-loader.lds-roller div:nth-child(7) {
  animation-delay: -0.252s;
}
.vb-loader.lds-roller div:nth-child(7):after {
  top: 63px;
  left: 17px;
}
.vb-loader.lds-roller div:nth-child(8) {
  animation-delay: -0.288s;
}
.vb-loader.lds-roller div:nth-child(8):after {
  top: 56px;
  left: 12px;
}
@keyframes lds-roller {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
</style>
