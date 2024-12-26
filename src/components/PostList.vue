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
          :key="post.id"
          @delete="$emit('delete', post)"
      />
  </div>
</template>

<style scoped>

</style>