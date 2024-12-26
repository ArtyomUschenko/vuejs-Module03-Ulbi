<script>
export default {
  name: 'MyButton'
}

</script>

<template>
  <button class="btn">
    <slot></slot>
  </button>
</template>

<style scoped>
  .btn {
    padding: 10px 15px;
    background: none;
    border-radius: 10px;
    border: 1px solid #446b5d;
    color: #446b5d;
    font-weight: bold;
    cursor: pointer;
  }
</style>