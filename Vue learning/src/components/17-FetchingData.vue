<!-- paihly api kk andrr data ko ham reponse ka use krky json mein convert kraingy pher osko responseData mein 
 laingy orr responseData ko data.value mein store krwa daingy orr screen prr dikha daingy.
-->

<script setup>
    import { ref } from 'vue';

    const data = ref(null)

    const FetchData = () => {
        fetch("https://jsonplaceholder.typicode.com/todos/1")
        .then((response) => {
            if(!response.ok) {
                throw new Error(`Https error ${response.status}`)
            }
            return response.json()
        })
        .then((responseData) => {
            data.value = responseData
        })
        .catch((error) => {
            console.error("error fetching data", error)
        })
    }
</script>

<template>
   
    <h2>Data from api</h2>
    <button @click="FetchData">Fetch</button>
    <pre>{{ data }}</pre>
</template>

<style scoped></style>