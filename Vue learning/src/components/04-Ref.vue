<script setup>
    import { ref } from 'vue';
    // 1.
    let count = ref(0)

    // 2.
    let userName = ref('')
</script>

<template>
    <!-- 1 -->
    <h1>Count is : {{ count }}</h1>
    <button @click="count++">+</button>
    <button @click="count--">-</button>


    <!-- 2 -->
     <h1>UserName is {{ userName }}</h1>
    <button @click="userName = 'Nasir'">Add Name</button>
</template>

<style scoped></style>