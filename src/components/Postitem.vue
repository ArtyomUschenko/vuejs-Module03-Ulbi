<script>
  export default {
    props: {
      post: {
        type: Object,
        required: true
      }
    }
  }
</script>

<template>
  <div class="post">
    <div>Название: <strong>{{ post.title }}</strong></div>
    <div>Описание: <strong>{{ post.body }}</strong></div>
  </div>
</template>

<style scoped>

</style>