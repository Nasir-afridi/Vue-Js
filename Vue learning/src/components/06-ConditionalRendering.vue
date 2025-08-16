<!-- if else-if else DOM mein tbhe ainge jbb wo true honge agrr wo false hain to dom mein nahe aainge -->

<script setup>
    const isTrue = false;
    const isFalse = false;
</script>


<template>
    <p v-if="isTrue">This is will something</p>
    <p v-else-if="isFalse">show me something</p>
    <p v-else>Nothing is true as false.</p>
</template>


<style scoped></style>