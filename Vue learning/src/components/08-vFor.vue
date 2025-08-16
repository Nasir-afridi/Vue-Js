
<script setup>
    import { ref } from 'vue';

    let people = ref(["Nasir", "Ali"]);
</script>

<template>
    <p v-for="person in people">{{ person }}</p>
</template>

<style scoped></style>