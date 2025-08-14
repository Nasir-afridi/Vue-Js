<template>


    <!-- 01-Text interpolation -->
     <h1>     
        Hello World {{ myMessage }}
        {{ 2 + 2 }} = {{ 22 + 22 }}
        <br>
        {{ add(2, 4)}}
    </h1>

    <!-- 02-attribute binding : for making the variable dynamic -->
     <a :href="myChannel">Youtube channel</a>       
     <img :src="Image" :width="ImageWidth" :height="ImageHeight" >


</template>


<script setup>

    // 01 - Text interpolation
    const myMessage = 'Yellow Color';
    function add (a, b ) {
        return a + b
    }

    // 02 - Attribute bindings Variable: 
    const myChannel = "https://www.youtube.com/watch?v=NcnfsE1B51o&list=PLEPye7A7EcQaJupAt4yTtJx3K-uUuj8si&index=3&ab_channel=SuperSimpleDev"
    const Image = "/favicon.ico"
    const ImageWidth = 400
    const ImageHeight = 400
</script>

<style scoped></style>