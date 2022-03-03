<template>
  <LoaderFacebook />
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import LoaderFacebook from './components/LoaderFacebook.vue';

export default defineComponent({
  name: 'App',
  components: {
    LoaderFacebook,
  },
});
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  background-color: #2c3e50;
}
</style>
