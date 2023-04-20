<!-- <script>
// use normal <script> to declare options
export default {
  inheritAttrs: false
}
</script> -->

<script setup>
import { ref } from "vue";
const email = ref('');
const password = ref('');
const emit = defineEmits({
    submitForm: (email,password) => {
        if(email && password){
            return true;
        }
        else{
            alert('please enter the email and password')
            return false
        }
    }
})
function onSubmit(email,password){
    emit('submitForm',email,password);
}
</script>

<template>
        <form name="login">
        <div class="col-6">
            <input name="email" v-model="email" class="form-control mt-2" placeholder="enter email" />
            <input name="password" v-model="password" class="form-control mt-3" placeholder="enter password" />
        </div>
        <button  @click.prevent="onSubmit( email, password)"  class="btn btn-success mt-3 ">Submit</button>
    </form>
</template>
