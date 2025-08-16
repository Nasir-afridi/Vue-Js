<script setup>
    const myMessage = 'Yellow Color';
    function add (a, b ) {
        return a + b
    }
</script>

<template>
    <h1>     
        Hello World {{ myMessage }}
        {{ 2 + 2 }} = {{ 22 + 22 }}
        <br>
        {{ add(2, 4)}}
    </h1>
</template>

<style scoped></style>