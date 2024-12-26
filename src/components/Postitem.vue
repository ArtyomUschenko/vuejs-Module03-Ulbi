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
    <div class="post__btns">
      <MyButton @click="$emit('delete')">Удалить</MyButton>
    </div>
  </div>

</template>

<style scoped>
  .post {
    padding: 15px;
    border: 2px solid #446b5d;
    margin-top: 15px;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
</style>