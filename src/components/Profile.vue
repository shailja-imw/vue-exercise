
<script setup>
defineProps(['profile']);
</script>

<template>
    <div class="img-avatar ">
        <img :src='profile.imgUrl' class="img-fluid object-fit-cover w-100 h-100" alt="avatar" />
    </div>
    <h3 class="mx-4 mb-0">{{ profile.name }}</h3>
</template>

<style>
.img-avatar {
    height: 74px;
    width: 74px;
    border-radius: 50%;
}
</style>
