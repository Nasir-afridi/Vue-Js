<script setup>
    // Example-1
    const value = defineProps(['firstName', 'lastName'])
</script>


<template>
    <!-- Example-1 -->
    <h1>First Name : {{ value.firstName }}</h1>
    <h1>Last Name : {{ value.lastName }}</h1>
</template>

j
<style scoped></style>