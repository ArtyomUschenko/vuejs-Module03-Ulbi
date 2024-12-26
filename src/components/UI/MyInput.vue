<script>
  export default {
    name: 'MyInput',
    props: {
      modelValue: [
          String, Number
      ]
    },
    methods:
    {
      updateInput(event) {
        this.$emit('update:modelValue', event.target.value)
      }
    },
  }
</script>

<template>
  <input class="input" type="text" :value="modelValue" @input="updateInput"/>
</template>

<style scoped>
  .input {
    width: 100%;
    border: 1px solid #446b5d;
    padding: 10px 15px;
    margin-top: 10px;
  }
</style>