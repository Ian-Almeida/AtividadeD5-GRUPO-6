<template>
  <div class="home">
    <div class="container" style="height: 200px; width: 200px; padding: 10px;">
      <div class="img-logo"> </div>
    </div>
    
    <nav class="navbar navbar-expand-lg navbar-light bg-light p-2">
      <a class="navbar-brand" href="#">Wxyz</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav mr-auto">
          <li class="nav-item active">
            <a class="nav-link" href="#">Início</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Grade Horária</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">
              Notas
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Mensagens</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Financeiro</a>
          </li>
        </ul>
        
      </div>
      
      <div class="dropstart">
        <button class="btn btn-text" type="button" data-bs-toggle="dropdown" aria-expanded="false">
          <span style="font-size: 16pt">. . .</span>
        </button>
        <ul class="dropdown-menu">
          <li><router-link class="dropdown-item" :to="{name: 'main-home-about'}">Sobre</router-link></li>
          <li><a class="dropdown-item pointer btn" @click="logout">Sair</a></li>
        </ul>
      </div>
    </nav>

    <router-view></router-view>
    
    
  </div>
</template>

<script lang="ts" setup>
import { useRouter } from "vue-router";

const router = useRouter();

function logout() {
  localStorage.loggedIn = 'false';
  router.push({name: 'main-login'});
}

</script>

<style scoped>
.img-logo {
  width: 200px;
  height: 200px;
  background-color: red;
}
</style>
