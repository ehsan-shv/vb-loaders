<template>
  <div class="control"><button @click="loading = !loading">disable/ enable loading</button></div>
  <section>
    <div class="container">
      <div>
        <LoaderFacebook />
        <h2>Facebook</h2>
      </div>
      <div>
        <LoaderDualRing />
        <h2>DualRing</h2>
      </div>
      <div>
        <LoaderCircle />
        <h2>Circle</h2>
      </div>
      <div>
        <LoaderRoller />
        <h2>Roller</h2>
      </div>
      <div>
        <LoaderRing />
        <h2>Ring</h2>
      </div>
      <div>
        <LoaderHeart />
        <h2>Heart</h2>
      </div>
      <div>
        <LoaderGrid />
        <h2>Grid</h2>
      </div>
      <div>
        <LoaderEllipsis />
        <h2>Ellipsis</h2>
      </div>
      <div>
        <LoaderDefault />
        <h2>Default</h2>
      </div>
      <div>
        <LoaderSpinner />
        <h2>Spinner</h2>
      </div>
      <div>
        <LoaderRipple />
        <h2>Ripple</h2>
      </div>
      <div>
        <LoaderHourglass />
        <h2>Hourglass</h2>
      </div>
    </div>
  </section>
  <div class="glass" />
  <LoaderContent class="blurLoaderContent" :disable="loading" :blur="true" innerLoader="LoaderSpinner">
    <div class="glass">
      <h2>blur</h2>
    </div>
  </LoaderContent>
  <LoaderContent innerLoader="LoaderSpinner" :disable="loading">
    <div class="glass">
      <h2>opacity</h2>
    </div>
  </LoaderContent>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'App',
  setup() {
    const loading = ref(true);
    return { loading };
  },
});
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fff;
  margin-top: 60px;

  & > div {
    margin: 40px 0;
  }

  section {
    margin-bottom: 80px;
    background-color: #2c3e50;
    display: flex;
    align-items: center;
    justify-content: center;

    .container {
      width: 300px;
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
      & > div {
        width: 80px;
        margin: 40px 0;
        h2 {
          font-size: 16px;
        }
      }
    }
  }

  .blurLoaderContent {
    --vb-loader-spinner-background-color: #212121;
  }

  .glass {
    height: 100vh;
    background-position: center bottom;
    background-size: cover;
    background-repeat: no-repeat;
    // background-image: url('assets/bg.jpg');
    display: flex;
    align-items: center;
    justify-content: center;

    h2 {
      font-size: 10vw;
    }
  }

  .control {
    position: fixed;
    top: 20px;
    right: 20px;
    padding: 20px;
    background-color: #fff;
    z-index: 99999;
    box-shadow: 0px 0px 9px 0px #21212185;
    border-radius: 4px;
  }
}
</style>
