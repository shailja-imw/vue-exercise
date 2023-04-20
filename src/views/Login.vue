<script setup>
import { ref } from 'vue';
import EmitValidation from '../components/EmitValidation.vue';
const isLoggedIn = ref(false);

const submitForm = (email, password) => {
    alert('Welcome ' + email + '\nYour Password is ' + password);
}

</script>


<template>
    <div class="container mt-5">
        <div class="alert alert-success mb-2" role="alert">
            <h4 class="alert-heading">{{ isLoggedIn ? "Well done!" : 'See You Soon' }}</h4>
            <p>{{ isLoggedIn ? 'Hooray !! You are now our member' : "we're Sorry to See you Go" }}</p>
        </div>
        <button v-if="isLoggedIn" @click="isLoggedIn = false" class="btn btn-success">Logout</button>
        <button v-else @click="isLoggedIn = true" class="btn btn-success">Login</button>

        <div v-if="!isLoggedIn">
            <EmitValidation @submit-form="submitForm" class="container mt-5" />
        </div>
    </div>
</template>
