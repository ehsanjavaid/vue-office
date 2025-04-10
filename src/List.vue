<template>
<div v-if="data">
    <ul>
      <Item v-for="item in data" :name="item.full_name" :img="item.image"/>
    </ul>
  </div>

</template>
<script setup>
import Item from './Item.vue'

import { ref, onMounted } from 'vue';

const data = ref(null);

const getoffice = "https://cors-anywhere.herokuapp.com/https://platform.buildwithhussain.dev/api/method/get-office";

onMounted(() => {
  fetch(getoffice)
    .then((d) => d.json())
    .then((message) => {
      // You have data
      data.value = message.data
    });
});
</script>