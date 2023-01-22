<template>
  <form @submit.prevent="user.login">
    <h1>Login</h1>
    <label>Username
      <input type="text" />
    </label>
    <label>
      Password
      <input type="password" />
    </label>
    <button>Login</button>
  </form>
</template>

<script setup lang="ts">
import { useUser } from '~~/stores/User';

const user=useUser()
definePageMeta({
  layout:'plain'
})
</script>

<style scoped>

</style>