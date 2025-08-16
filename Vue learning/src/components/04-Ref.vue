<!-- Ref mein ham primitive data types or object array saab kk sath kaam krskty hain ismein aik special box banjata hai jisko
 ham .value kaihty hain yane koi be value access krne ho to isko likhty hain last mein function kkk andrr orr agrr eventhandler
 use krrhy ho to pher vue isko automaticlly unwrap krdaita hai isko likhny kii zroorat nahe leken function mein must wrna ye 
 error dyga. -->

<script setup>
    import { ref } from 'vue';
    // 1.
    let count = ref(0)

    // 2.
    let userName = ref('')

    // 3.
    let obj = ref({
        names: "Nasir",
        age : 30
    })

    function nameChange() {
        if(obj.value.names === "Nasir" && obj.value.age === 30) {
            obj.value.names = "ali"
            obj.value.age= 20
        }else {
            obj.value.names= "Nasir",
           obj.value.age = 30
        }
    }
</script>

<template>
    <!-- 1 -->
    <h1>Count is : {{ count }}</h1>
    <button @click="count++">+</button>
    <button @click="count--">-</button>


    <!-- 2 -->
     <h1>UserName is {{ userName }}</h1>
    <button @click="userName = 'Nasir'">Add Name</button>


    <!-- 3 -->
     <h1>User name is : {{ obj.names}}</h1>
     <h1>User age is : {{ obj.age }}</h1>

     <button @click="nameChange">change the user</button>
</template>

<style scoped></style>