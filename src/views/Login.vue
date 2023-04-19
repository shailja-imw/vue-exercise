<script setup>
import { ref } from 'vue';
const isLoggedIn = ref(false);

</script>


<template>
    <div class="container mt-5">
        <div class="alert alert-success mb-2" role="alert">
            <h4 class="alert-heading">{{ isLoggedIn ? "Well done!" : 'See You Soon'}}</h4>
            <p>{{ isLoggedIn ? 'Hooray !! You are now our member' : "we're Sorry to See you Go" }}</p>
        </div>
        <button v-if="isLoggedIn" @click="isLoggedIn = false" class="btn btn-success">Logout</button>
        <button v-else @click="isLoggedIn = true" class="btn btn-success">Login</button>
    </div>
</template>
