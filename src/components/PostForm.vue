<script setup>

</script>

<template>
  <form @submit.prevent>
    <h4>Создание поста</h4>
    <input class="input" type="text" placeholder="Название" v-bind:value="title" @input="title=$event.target.value">
    <input class="input" type="text" placeholder="Описание" v-bind:value="body" @input="body=$event.target.value">
    <button class="btn" >Создать</button>
  </form>
</template>

<style scoped>
  form {
    display: flex;
    flex-direction: column;
  }
  .btn {
    padding: 10px 15px;
    background: none;
    border-radius: 10px;
    border: 1px solid #446b5d;
    align-self: flex-end;
    margin-top: 10px;
    color: #446b5d;
    font-weight: bold;
    cursor: pointer;
  }
  .input {
    width: 100%;
    border: 1px solid #446b5d;
    padding: 10px 15px;
    margin-top: 10px;
  }
</style>