<template>
  <section>
    <div><LoaderFacebook /></div>
    <div><LoaderDualRing /></div>
    <div><LoaderCircle /></div>
    <div><LoaderRoller /></div>
    <div><LoaderRing /></div>
    <div><LoaderHeart /></div>
    <div><LoaderGrid /></div>
    <div><LoaderEllipsis /></div>
    <div><LoaderDefault /></div>
    <div><LoaderSpinner /></div>
    <div><LoaderRipple /></div>
    <div><LoaderHourglass /></div>
  </section>
  <div class="glass" />
  <LoaderContent :blur="true">
    <div class="glass" />
  </LoaderContent>
  <LoaderContent>
    <div class="glass" />
  </LoaderContent>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import LoaderCircle from './components/LoaderCircle.vue';
import LoaderFacebook from './components/LoaderFacebook.vue';
import LoaderDualRing from './components/LoaderDualRing.vue';
import LoaderRoller from './components/LoaderRoller.vue';
import LoaderRing from './components/LoaderRing.vue';
import LoaderHeart from './components/LoaderHeart.vue';
import LoaderGrid from './components/LoaderGrid.vue';
import LoaderEllipsis from './components/LoaderEllipsis.vue';
import LoaderDefault from './components/LoaderDefault.vue';
import LoaderSpinner from './components/LoaderSpinner.vue';
import LoaderRipple from './components/LoaderRipple.vue';
import LoaderHourglass from './components/LoaderHourglass.vue';
import LoaderContent from './components/LoaderContent.vue';

export default defineComponent({
  name: 'App',
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
    LoaderContent,
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

  & > div {
    margin: 40px 0;
  }

  section {
    margin-bottom: 80px;
    background-color: #2c3e50;
  }

  .glass {
    height: 100vh;
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    background-image: url(https://images.unsplash.com/photo-1646316924344-8e162ab28cfe?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80);
  }
}
</style>
