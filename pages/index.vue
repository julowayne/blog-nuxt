<template>
  <div>
    <div class="about mt-24">
      <h4 class="text-3xl">
        Welcome to our blog<div class="p-3">
          <img class="rounded shadow" src="https://media.giphy.com/media/MJQJow1uUbNDy/giphy.gif" alt="welcome gif">
        </div> You can go to <NuxtLink id="posts" to="/posts">
          our posts page
        </NuxtLink> to discover everything.
      </h4>
    </div>
  </div>
</template>

<script>
export default {
  head: {
    title: 'Mon blog',
    meta: [
      { charset: 'utf-8' },
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      {
        hid: 'description',
        name: 'description',
        content: 'Accueil du blog'
      }
    ],
    link: [{ rel: 'icon', type: 'image/x-icon', href: '/favicon-32x32.png' }]
  }
}
</script>

<style>
 .about {
  display: flex;
  justify-content: center;
  text-align: center;
}
#posts {
  color:#6610f2;
  font-style: italic;
}
img {
  margin: 0 auto;
}
</style>
