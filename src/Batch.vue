<template>
<div :class='[
    "bg-green-500 text-white text-xl",
    statusToClasses[color],
    ]'>
    {{ props.status }}
</div>

</template>
<script setup>
import { computed } from 'vue'
const statusToClasses = {
    "green": 'text-green-500 bg-green-100',
    "red": 'text-red-500 bg-red-100',
    "yellow": 'text-yellow-500 bg-yellow-100',
}
const statusToColor = {
    Active: 'green',
    Inactive: 'red',
    Pending: 'yellow',
}
const props = defineProps({
    status: String
})

const color = computed(() => {
    return statusToColor[props.status]
})
</script>