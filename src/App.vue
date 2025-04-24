<template>
  <Badge @click="showConfetti" :variant="'subtle'" :ref_for="true" theme="green" size="lg" label="Badge">
    Badge
  </Badge>
  <Badge @click="showDialog = true" :variant="'subtle'" :ref_for="true" theme="green" size="lg" label="Badge">
    Show Dialog
  </Badge>
  
  <Dialog v-model="showDialog" :options="{
    title: 'Confirm',
    message: 'Are you sure you want to confirm this action?',
    size: 'xl',
  }" />
</template>
<script setup>
import Badge from 'frappe-ui/src/components/Badge.vue';
import Dialog from 'frappe-ui/src/components/Dialog.vue';
import confetti from 'canvas-confetti';
// import { Badge, Dialog, Button } from 'frappe-ui';
// import { dialogs } from 'frappe-ui/src/utils/confirmDialog';
import { ref } from 'vue';
const showDialog = ref(false);
function showConfetti() {
  confetti({
    particleCount: 200,
    spread: 90,
    origin: { y: 0.8 }
  });
}
</script>
<style></style>