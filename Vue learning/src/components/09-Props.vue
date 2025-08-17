<!-- sending data from the parent component to the child component -->

<script setup>
    let value = defineProps(['name'])
    console.log(value)
</script>


<template>
    <h1>{{ value.name }}</h1>
</template>


<style scoped></style>