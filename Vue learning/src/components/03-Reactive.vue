<script setup>
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

    // Reactive Example-02
    let newState = reactive({val : {counter : 0}, users : ["nasir", "ali"]})
    function countNumber() {
        newState.val.counter++
    }
    function changeUsers() {
        newState.users[0] = "Muhammad"
        newState.users[1] = "Ali"
    }
    function addUsers() {
        newState.users.push("Nasir Khan")
    }
</script>


<template>
     <!-- 03 - Reactive Example-1 -->
    <p>Count is : {{ state.count }}</p>
    <p>Name is : {{ state.user.name }}</p>
    <p>Age is : {{ state.user.age }}</p>
    <button @click="countUpdate">Count</button>
    <button @click="update">Change Name</button>

    <!-- 03 - Reactive Example-2 -->
    <h1>Count is {{ newState.val.counter }}</h1>
    <h2>Name are : {{ newState.users }}</h2>

    <button @click="countNumber">Counter</button>
    <button @click="changeUsers">Change User</button>
    <button @click="addUsers">Add users</button>
</template>


<style scoped></style>