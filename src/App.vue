<template>
<Badge
@click="showConfetti"
  :variant="'subtle'"
  :ref_for="true"
  theme="green"
  size="lg"
  label="Badge"
>
  Badge
</Badge>
</template>
<script setup>
import Badge from 'frappe-ui/src/components/Badge.vue';
import confetti from 'canvas-confetti';
function showConfetti() {
  confetti({
    particleCount: 200,
    spread: 90,
    origin: { y: 0.8 }
  });
}
</script>
<style></style>