<template>
<div class="container">
  <div class="card">
    <div class="card-body">
      <h3>Faça seu login</h3>
      <form @submit="submitLogin">
        <div class="mb-3">
          <label for="inputEmail" class="form-label">Email</label>
          <input v-model="loginInput.email" type="email" class="form-control" id="inputEmail" aria-describedby="emailHelp" required>
        </div>
        <div class="mb-3">
          <label for="inputPassword" class="form-label">Senha</label>
          <input v-model="loginInput.pwd" type="password" class="form-control" id="inputPassword" required>
        </div>
        <button type="submit" class="btn btn-primary">Entrar</button>
      </form>
    </div>
  </div>
  
</div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import { useRouter } from 'vue-router';

const router = useRouter();
const loginInput = ref({email: '', pwd: ''});

function submitLogin() {
  localStorage.loggedIn = 'true';
  router.push({name: 'main-home'});
}

</script>

<style scoped>
h3 {
  text-align: center;
  font-weight: bold;
}
</style>
