<template>
  Explicit imports:
  <div>
    <HelloFromMain />
    <HelloFromLibManually />
    <HelloFromLibVue />
  </div>
  Automatic imports:
  <div>
    <UnimportedHelloFromMain />
    <UnimportedHelloFromLib />
  </div>

  Wildcard imports:
  <div>
    <h1>{{ retTest() }}</h1>
    <h1>{{ otherTest() }}</h1>
  </div>
</template>

<script setup lang="ts">
import { retTest } from '@/common/test';
import { otherTest } from '@unplugin-components-monorepo/libcomponents/common/test.ts';
import HelloFromMain from '../components/HelloFromMain.vue';
import { HelloFromLib as HelloFromLibManually } from '@unplugin-components-monorepo/libcomponents';
import HelloFromLibVue from '@unplugin-components-monorepo/libcomponents/components/HelloFromLib.vue';
</script>
