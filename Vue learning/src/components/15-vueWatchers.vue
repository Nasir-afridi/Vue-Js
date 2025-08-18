<!-- 
 Watcher : 
Data ko watch karta hai (matlab reactive variable / prop)

Agar us data me change aata hai → turant react karta hai

Aur tumhari likhi hui function / logic run kar deta hai 
-->

<script setup>
    import { watch, ref } from 'vue';
    const message = ref("hello")
    const input = ref('')


    watch(input, (newValue, oldValue) => {
        message.value = `You typed : ${newValue}`
    })
</script>

<template>
    <h1>{{ message }}</h1>
    <input v-model="input" placeholder="type something here" type="text">
</template>

<style scoped>

</style>