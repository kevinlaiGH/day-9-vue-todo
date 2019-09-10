<template>
  <div>
    <input
      type="text"
      class="todo-input"
      placeholder="what needs to be done"
      v-model="newTodo"
      @keyup.enter="addTodo"
    />
    TodoList goes here
    <div v-for="todo in todos" :key="todo.id" class="todo-item">{{todo.title}}</div>
  </div>
</template>

<script>
export default {
  name: "todo-list",
  data() {
    return {
      newTodo: "",
      idForTodo: 3,
      todos: [
        {
          id: 1,
          title: "finished first one",
          completed: false
        },
        {
          id: 2,
          title: "finished 2nd one",
          completed: true
        }
      ]
    };
  },
  methods: {
    addTodo() {
      this.todos.push({
        id: this.idForTodo,
        title: this.newTodo,
        completed: false
      });
      this.newTodo = "";
      this.idForTodo++;
    }
  }
};
</script>

<style lang="scss">
.todo-input {
  width: 100%;
  padding: 10px 18px;
  font-size: 18px;
  margin-bottom: 16px;
  border-color: black;
  border-radius: 30px;

  &:focus {
    outline: 0;
  }
}
.todo-item {
  margin-bottom: 12px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  animation-duration: 0.3s;
}
</style>
