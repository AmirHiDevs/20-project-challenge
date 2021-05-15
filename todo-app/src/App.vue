<template>
  <div >
    <todos v-bind:todos="todos" />
    <add-todo @emit-Addtodo="addTodo"/>
  </div>
</template>

<script>
import Todos from "./components/Todos";
import addTodo from "./components/addTodo";

export default {
  name: "app",
  components: {
    Todos,
    addTodo, 
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: "discussion with jalal about vue",
          completed: false,
        },
        {
          id: 2,
          title: "to-do app proj",
          completed: false,
        },
        {
          id: 3,
          title: "doing 3",
          completed: false,
        },
        {
          id: 4,
          title: "dojng 4",
          completed: false,
        },
        {
          id: 5,
          title: "doing 5",
          completed: false,
        },
        {
          id: 6,
          title: "doing 6",
          completed: false,
        },
      ],
    };
  },


  methods:{
    addTodo(newTodo){
      this.todos.push(newTodo)
    }
  }
};


</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
