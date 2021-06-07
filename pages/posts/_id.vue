<template>
  <div class="post">
    <Post :post="post" />
  </div>
</template>

<script>
export default {
  data () {
    return {
      post: []
    }
  },
  async fetch () {
    this.post = await fetch(`https://jsonplaceholder.typicode.com/posts/${this.$route.params.id}`).then(res =>
      res.json())
  },
  head: {
    title: 'My post',
    meta: [
      { charset: 'utf-8' },
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      {
        hid: 'description',
        name: 'description',
        content: 'My post content'
      }
    ],
    link: [{ rel: 'icon', type: 'image/x-icon', href: '/favicon-32x32.png' }]
  }
}
</script>

<style>

.post {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  text-align: left;
  max-width: 600px;
}
.title {
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
  text-align: center;
}
</style>
