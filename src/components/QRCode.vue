<script setup lang="ts">
import { ref } from 'vue';
// defineProps<{ qrCode: string }>();
import '@shoelace-style/shoelace/dist/components/button/button.js';
import '@shoelace-style/shoelace/dist/components/icon/icon.js';
import '@shoelace-style/shoelace/dist/components/input/input.js';
import '@shoelace-style/shoelace/dist/components/rating/rating.js';
import '@shoelace-style/shoelace/dist/components/qr-code/qr-code.js';
import '@shoelace-style/shoelace/dist/components/input/input.js';

const qrCode = ref();
</script>

<template>
  <div class="container">
    <h1>QR code generator</h1>

    <sl-input
      maxlength="255"
      clearable
      label="Value"
      v-model="qrCode"
    ></sl-input>

    <sl-qr-code :value="qrCode"></sl-qr-code>

    <sl-button variant="primary" pill onclick="alert('shoelace');">
      <sl-icon slot="prefix" name="gear"></sl-icon>
      Shoelace Settings
    </sl-button>
  </div>
</template>

<style>
.container {
  max-width: 400px;
  margin: 0 auto;
}

sl-input {
  margin: var(--sl-spacing-large) 0;
}
</style>
