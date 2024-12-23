<template>
  <div class="app">

  </div>
</template>
<script>
import PostForm from "@/components/PostForm.vue";
import PostList from "@/components/PostList.vue";
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
</style>