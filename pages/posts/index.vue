<template>
  <div class="container">
    <div>
      <h1 class="title">
        Mes posts
      </h1>
      <div v-if="posts.length">
        <div v-for="post in posts" :key="post">
          <NuxtLink :to="`/posts/${post.id}`">
            <span class="font-bold">{{ post.id }}.</span> {{ post.title }}
          </NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData ({ params, $http }) {
    const posts = await $http.$get('https://jsonplaceholder.typicode.com/posts')
    return { posts }
  },
  data () {
    return {
      posts: []
    }
  },
  head: {
    title: 'Les posts',
    meta: [
      { charset: 'utf-8' },
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      {
        hid: 'description',
        name: 'description',
        content: 'Posts du blog'
      }
    ],
    link: [{ rel: 'icon', type: 'image/x-icon', href: '/favicon-32x32.png' }]
  }
}
</script>

<style>

.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

</style>
