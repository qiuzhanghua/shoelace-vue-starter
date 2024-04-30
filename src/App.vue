<script setup lang="ts">
import '@shoelace-style/shoelace/dist/themes/light.css';
import { setBasePath } from '@shoelace-style/shoelace/dist/utilities/base-path.js';
setBasePath('/');

import QRCode from './components/QRCode.vue';
</script>

<template>
  <div>
    <QRCode />
  </div>
</template>

<style scoped>
</style>
