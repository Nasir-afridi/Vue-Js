
<script setup>
    // Example : 1
    import { ref } from 'vue';
    let people = ref(["Nasir", "Ali"]);

    // Example : 2
    let name = ref(["khan", "malik"]);
</script>

<template>
    <!-- Example-1 -->
    <p v-for="person in people">{{ person }}</p>

    <!-- Example-2 -->
    <p v-for=" (names,index) in name" :key="index">{{index}}  {{names}} </p>
</template>

<style scoped></style>