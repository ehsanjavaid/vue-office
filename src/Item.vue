<template>
<h1>{{ props.name }}</h1>
<img style="height: 100px; display: block; padding-bottom: 20px; padding-top: 20px;" :src="props.img" alt="">
</template>
<script setup>
const props = defineProps({
    name: String,
    img: String
})
</script>