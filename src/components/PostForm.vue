<script>

import MyInput from "@/components/UI/MyInput.vue";

export default {
  components: {MyInput},
 data() {
   return {
     post: {
       title: '',
       body: ''
     }
   }
 },
  methods: {
    createPost() {
      this.post.id = Date.now();
      this.$emit("create", this.post);
      this.post = {
        title: '',
        body: ''
      }
    }
  }

}

</script>

<template>
  <form @submit.prevent>
    <h4>Создание поста</h4>
    <MyInput type="text" placeholder="Название"
    v-model="post.title"/>
    <MyInput type="text" placeholder="Описание"
             v-model="post.body" />
    <MyButton class="btn" @click="createPost">Создать</MyButton>
  </form>
</template>

<style scoped>
  form {
    display: flex;
    flex-direction: column;
  }
  .btn {
    align-self: flex-end;
    margin-top: 10px;
  }

</style>
