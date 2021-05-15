<template>
  <div>
    <input type="text" v-model="title" name="title" />
    <button type="submit" @click="addTodo">Add</button>
  </div>
</template>

<script>
export default {
  name: "AddTodo",
  data() {
    return {
      title: "",
    };
  },

  methods: {
    randomId() {
      return Math.ceil(Math.random() * 100000);
    },
    addTodo() {
      const newTodo = {
        id: this.randomId(),
        title: this.title,
        completed: false,
      };

      this.$emit('emit-Addtodo',newTodo);
      this.title = "";
    },
  },
};
</script>

<style></style>
