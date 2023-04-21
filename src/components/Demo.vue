<script setup>
import { ref,reactive,computed } from 'vue';
const name = ref('shailja');
const sum1 = ref(0);
const sum2= ref(0);
const array = reactive([1,2,3,4,5,6,7,8,9,10]);

const result = computed(()=>{
    return sum1.value * sum2.value
})
</script>
<template>
<div class="name">{{ name }}</div>
<div v-for="arr in array">
{{ arr }}
</div>
<input v-model="sum1"/>
<input v-model="sum2"/>
<div>{{ result }}</div>
<h1>{{ name }}</h1>
</template>

<style>
.name{
    color:red;
}
</style>
