<!-- Data ko html sy connect krny kk liye hota hia takay data mein koi change ho to html osko foraan trigger
 kray orrr ui update krday yane hamain html mein change na krna paray -->

<script setup>
    const myChannel = "https://www.youtube.com/watch?v=NcnfsE1B51o&list=PLEPye7A7EcQaJupAt4yTtJx3K-uUuj8si&index=3&ab_channel=SuperSimpleDev"
    const Image = "/favicon.ico"
    const ImageWidth = 400
    const ImageHeight = 400
</script>

<template>
    <a :href="myChannel">Youtube channel</a>       
    <img :src="Image" :width="ImageWidth" :height="ImageHeight" >
</template>

<style scoped></style>