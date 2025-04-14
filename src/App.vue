<template>

  <div style="margin: 10px">
    <button @click="showConfetti" style="background-color: black; color: white; padding: 15px; border-radius: 10px ;">Confetti</button>
  </div>
 
</template>
<script setup>
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