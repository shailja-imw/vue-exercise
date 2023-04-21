<script setup>
import { RouterLink, RouterView } from 'vue-router'

import Header from './components/Header.vue';
import Profile from './components/Profile.vue';
import userAvtar from './assets/Images/man.png'
import Logo from './assets/Images/logo.png'
const profile = {
  imgUrl: userAvtar,
  name: 'Marry Jack'
}
</script>

<template>
  <nav class="navbar navbar-expand-lg navbar-ligt bg-light">
    <div class="container-fluid">
      <img :src='Logo' class="img-fluid logo mx-4" />
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse order-sm-2" id="navbarSupportedContent">
        <Header></Header>
        <form class="d-flex justify-content-center align-items-center cursor-pointer order-sm-1">
          <Profile v-bind:profile="profile"></Profile>
        </form>
      </div>
    </div>
  </nav>
  <RouterView />
</template>

<style>
.logo {
  height: 74px;
}
@media screen and (max-width:767px) {
  .logo{
    height: 40px;
  }
}
</style>
