<template>
  <div id="app" class="container">
    <HelloWorld />
    <TodoList />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import TodoList from "./components/TodoList.vue";
export default {
  name: "app",
  components: {
    HelloWorld,
    TodoList
  }
};
</script>

<style>
* {
  box-sizing: border-box;
}

.container {
  max-width: 600px;
  margin: 0 auto;
}

.App-logo {
  /* animation: App-logo-spin infinite 20s linear; */
  height: 20vmin;
  float: left;
  margin: auto;
  width: 50%;
}

/* @keyframes App-logo-spin {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
} */

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
