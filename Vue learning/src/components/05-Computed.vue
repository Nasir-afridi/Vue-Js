

<!-- Computed: do ya do sy zyada ref / reactive ko aik banana jaisy first name + lastname ko aik final fullName variable mein lana -->



<script setup>
    import { computed, ref } from 'vue';

    const firstName = ref("Nasir");
    const lastName = ref("khan");
    const fullName = computed(() => firstName.value + " " + lastName.value)
</script>



<template>
    <h1>Full Name is {{ fullName }}</h1>
</template>



<style scoped></style>