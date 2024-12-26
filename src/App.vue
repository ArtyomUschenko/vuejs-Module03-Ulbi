<template>
  <div class="app">
      <PostForm   @create="createPost"/>
      <PostList :posts="posts"
      @delete="deletePost"/>
  </div>
</template>
<script>
import PostForm from "@/components/PostForm.vue";
import PostList from "@/components/PostList.vue";
  export default {
    components: { PostForm, PostList},
    data() {
      return {
        posts : [
          {id: 1, title: "ЭД", body: "Описание поста"},
          {id: 2, title: "ЭД 2", body: "Описание поста 2"},
          {id: 3, title: "ЭД 3", body: "Описание поста 3"},
        ],
      }
    },
    methods:
    {
      createPost(post){
        this.posts.push(post);
      },
      deletePost(post) {
        this.posts = this.posts.filter(p => p.id !== post.id);
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