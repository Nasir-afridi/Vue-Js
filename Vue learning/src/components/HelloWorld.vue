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


    // 03 Reactive:  Example1
    import { reactive } from 'vue';
    let state = reactive({count : 0, user : {name : 'Nasir', age : 20}})
    function countUpdate(){
        state.count++
    }
    function update() {
        if(state.user.name === "Nasir") {
            state.user.name = "ali"
            state.user.age = 90
        }else {
            state.user.name = 'Nasir'
            state.user.age =20
        }
        
    }

</script>



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


    <!-- 03 - Reactive Example 1 -->
    <p>Count is : {{ state.count }}</p>
    <p>Name is : {{ state.user.name }}</p>
    <p>Age is : {{ state.user.age }}</p>
    <button @click="countUpdate">Count</button>
    <button @click="update">Change Name</button>
    
</template>



<style scoped></style>
