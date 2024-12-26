<script>
  import Postitem from "@/components/Postitem.vue";

  export default
  {
    components: {Postitem},
    props: {
      posts: {
        type: Array,
        required: true
      }
    }
  }

</script>

<template>
  <div class="">
      <h3>Список пользователей</h3>
      <postitem
          v-for="post in posts"
          :post="post"
      />
  </div>
</template>

<style scoped>
.post {
  padding: 15px;
  border: 2px solid #446b5d;
  margin-top: 15px;
}
</style>