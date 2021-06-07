<template>
  <div>
    <h1 class="title mb-3">
      Mon post
    </h1>
    <div class="text-2xl body shadow p-5">
      <div class="p-1 text-3xl content">
        Content :
      </div>
      <div class="p-3">
        {{ post.body }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Post',
  props: ['post'],
  data () {
    return {
      description: 'A blog post about some stuff'
    }
  }
}
</script>
<style scoped>
.body {
  background-color: white;
  border-radius: 3px;
}
.content {
  border-bottom: 1px solid grey;
  width: 25%;
}
</style>
