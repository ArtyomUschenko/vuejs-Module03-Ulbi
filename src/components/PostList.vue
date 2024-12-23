<script setup>

</script>

<template>
  <div class="post" v-for="post in posts">
    <div>Название: <strong>{{ post.title }}</strong></div>
    <div>Описание: <strong>{{ post.body }}</strong></div>
  </div>
</template>

<style scoped>
.post {
  padding: 15px;
  border: 2px solid #446b5d;
  margin-top: 15px;
}
</style>