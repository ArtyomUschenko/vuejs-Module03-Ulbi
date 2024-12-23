<template>
  <div class="app">
    <form @submit.prevent>
      <h4>Создание поста</h4>
      <input class="input" type="text" placeholder="Название" v-bind:value="title" @input="title=$event.target.value">
      <input class="input" type="text" placeholder="Описание" v-bind:value="body" @input="body=$event.target.value">
      <button class="btn" @click="createPost()">Создать</button>
    </form>
    <div class="post" v-for="post in posts">
      <div>Название: <strong>{{ post.title }}</strong></div>
      <div>Описание: <strong>{{ post.body }}</strong></div>
    </div>
  </div>
</template>


<script>
  export default {
    data() {
      return {
        posts : [
          {id: 1, title: "ЭД", body: "Описание поста"},
          {id: 2, title: "ЭД 2", body: "Описание поста 2"},
          {id: 3, title: "ЭД 3", body: "Описание поста 3"},
        ],
        title: "",
        body: "",
      }
    },
    methods:
    {
      createPost(){
        const newPost = {
          id: Date.now(),
          title: this.title,
          body: this.body,
        }
        this.posts.push(newPost)
        this.title = "";
        this.body = "";
      }
    }
  }
</script>



<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.app {
  padding: 20px;
}
.post {
  padding: 15px;
  border: 2px solid #446b5d;
  margin-top: 15px;
}
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