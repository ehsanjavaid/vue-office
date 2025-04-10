<template>
  
  <h1 class="text-bold">helo</h1>
  <input v-model="Value" type="text" name="" id="">
  <input v-model="document" type="text" name="" id="">
  <List />
  <div class="bg-red-500 p-4 text-white">
  Test Tailwind - this should be red
</div>
</template>
<script setup>
import List from './List.vue'
import { ref, watch } from 'vue';
const Value = ref("")
const document = ref("")
watch(Value, (newValue, oldValue)=> {
  console.log(`Value changed from ${oldValue} to ${newValue}`);
  document.value = newValue
  console.log(document.value);
  
})
</script>
<style></style>