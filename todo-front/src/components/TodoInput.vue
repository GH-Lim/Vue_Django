<template>
  <div class="todo-input">
    <form class="input-group mb-3" @submit.prevent="onSubmit">
      <input type="text" class="form-control" v-model="title">
      <button class="btn btn-success" type="submit">add</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'TodoInput',
  data() {
    return {
      title: ''
    }
  },
  methods: {
    onSubmit() {
      this.$emit('createTodo', this.title)
      this.title = ''
    }
  }
}
</script>

<style>

</style>