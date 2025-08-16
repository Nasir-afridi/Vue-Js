<!-- vShow dom mein hamesha addd rhta hai beshak true ho ya false agrr true hai to show hoga agrr false hai to hide hoga -->

<script setup>
    import { ref } from 'vue';
    let showMessage = ref(true);
</script>

<template>
    <p v-show="showMessage">This is Paragraph</p>
    <button @click="showMessage = !showMessage">toggle button</button>
</template>

<style scoped></style>