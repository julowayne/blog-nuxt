<template>
  <div class="container">
    <h2 v-if="error.statusCode === 404" class="text-3xl font-bold">
      Page not found
    </h2>
    <h1 v-else>
      Une erreur est survenue
    </h1><br>
    <img src="https://media.giphy.com/media/YAlhwn67KT76E/source.gif" class="rounded shadow" alt="404 gif">
    <div class="text-3xl font-bold">
      404
    </div>
    <NuxtLink id="home" class="text-4xl mt-5" to="/">
      Get back to home
    </NuxtLink>
  </div>
</template>

<script>
export default {
  layout: 'blog',
  props: ['error'],
  head: {
    title: 'Error',
    meta: [
      { charset: 'utf-8' },
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      {
        hid: 'description',
        name: 'description',
        content: 'Error'
      }
    ],
    link: [{ rel: 'icon', type: 'image/x-icon', href: '/warning.png' }]
  }
  // you can set a custom layout for the error page
}
</script>
<style>

body {
  background-color: #f8f9fa;
}
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}
#home {
  text-decoration: underline;
  font-style: italic;
  color: grey;
}

</style>
