<template>
  <nav class="flex justify-around shadow content-center">
    <NuxtLink class="text-2xl p-3 font-bold" to="/">
      Home
    </NuxtLink>
    <NuxtLink class="text-2xl p-3 font-bold" to="/posts">
      Posts
    </NuxtLink>
    <NuxtLink class="text-2xl p-3 font-bold" to="/about">
      About
    </NuxtLink>
  </nav>
</template>

<script>
export default {
  name: 'Navigation'
}
</script>

<style>
nav {
  background-color: #007bff;
}
</style>
