<template>
  <div class="vb-loader lds-dual-ring" />
</template>

<style lang="scss">
:root {
  --vb-loader-dual-ring-background-color: #ffffff;
}
.vb-loader.lds-dual-ring {
  display: inline-block;
  width: 80px;
  height: 80px;
}
.vb-loader.lds-dual-ring:after {
  content: ' ';
  display: block;
  width: 64px;
  height: 64px;
  margin: 8px;
  border-radius: 50%;
  border: 6px solid var(--vb-loader-dual-ring-background-color);
  border-color: var(--vb-loader-dual-ring-background-color) transparent var(--vb-loader-dual-ring-background-color)
    transparent;
  animation: lds-dual-ring 1.2s linear infinite;
}
@keyframes lds-dual-ring {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
</style>
