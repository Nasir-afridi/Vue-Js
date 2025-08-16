<!-- vShow dom mein hamesha addd rhta hai beshak true ho ya false agrr true hai to show hoga agrr false hai to hide hoga -->

<script setup>
    let showMessage = false;
</script>

<template>
    <p v-show="showMessage">This is Paragraph</p>
</template>

<style scoped></style>