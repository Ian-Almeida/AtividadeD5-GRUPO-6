<template>
  <router-view/>
</template>

<script setup lang="ts">

import {onBeforeMount} from "vue";
import {useRouter} from "vue-router";

const router = useRouter();


onBeforeMount(() => {
  if (localStorage?.loggedIn) {
    if (localStorage.loggedIn === 'false') router.push({name: 'main-login'});
    else if (!router.currentRoute.value.fullPath.includes('/home')) router.push({name: 'main-home'});
  } else {
    router.push({path: '/login'});
  }

})
</script>

<style scoped>

</style>
