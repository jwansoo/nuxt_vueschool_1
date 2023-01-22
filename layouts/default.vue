<template>
  <div> 
    <nav stype="display: flex;gap:10px;">
      <NuxtLink to="/">Home</NuxtLink>
      <NuxtLink to="/movies">Movies</NuxtLink>
      <NuxtLink to="https://vueschool.id">Vue School</NuxtLink>
      <NuxtLink v-if="!user.isLoggedIn" to="/login">Login</NuxtLink>
      <a href="#" v-else @click.prevent="user.isLoggedIn=false">Logout</a>
      Test
    </nav>
    <slot></slot>
  </div>
</template>
<script setup lang="ts">
const user=useUser()
</script>