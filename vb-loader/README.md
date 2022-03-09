# vb-loader

<a href="https://www.npmjs.com/package/vb-loader"><img src="https://img.shields.io/npm/v/vb-loader.svg" alt="Version"></a>

> Loader components for Vue3. [Demo](https://ehsan-shv.github.io/vb-loader/)

## Components

- LoaderFacebook
- LoaderDualRing
- LoaderCircle
- LoaderRoller
- LoaderRing
- LoaderHeart
- LoaderGrid
- LoaderEllipsis
- LoaderDefault
- LoaderSpinner
- LoaderRipple
- LoaderHourglass
- LoaderContent

## Installation

```
npm i vb-loaders
```

## Example

```vue
<template>
  <LoaderRoller />
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import { LoaderRoller } from 'vb-loaders';

export default defineComponent({
  components: {
    LoaderRoller,
  },
});
</script>
```

## Content Loader Example

```vue
<template>
  <LoaderContent :disable="loading" :blur="true" innerLoader="LoaderSpinner">
    <div>
      <h1>Hello World!</h1>
    </div>
  </LoaderContent>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import { LoaderContent } from 'vb-loaders';

export default defineComponent({
  components: {
    LoaderContent,
  },
  setup() {
    const loading = ref(true);
    return { loading };
  },
});
</script>
```
