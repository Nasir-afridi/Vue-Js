<template>
    <h1>
        Hello World {{ myMessage }}
        {{ 2 + 2 }} = {{ 22 + 22 }}
        <br>
        {{ add(2, 4)}}
    </h1>

     <a :href="myChannel">Youtube channel</a>       <!--attribute binding : for making the variable dynamic -->
     <img :src="Image" :width="ImageWidth" :height="ImageHeight" >
</template>

<script setup>

    const myMessage = 'Yellow Color';
    function add (a, b ) {
        return a + b
    }

    const myChannel = "https://www.youtube.com/watch?v=NcnfsE1B51o&list=PLEPye7A7EcQaJupAt4yTtJx3K-uUuj8si&index=3&ab_channel=SuperSimpleDev"
    const Image = "/favicon.ico"
    const ImageWidth = 400
    const ImageHeight = 400
</script>

<style scoped></style>