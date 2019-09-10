<template>
  <div class="hello">
    <h1>{{ user }}</h1>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'HelloWorld',
  data: function() {
  return {
      user: "Nothing :(",
      errors: [],
  };
 },
 created() {
    axios.get(`https://todoapp-252506.appspot.com/users`)
    .then(response => {
      // JSON responses are automatically parsed.
      this.user = response.data
    })
    .catch(e => {
      this.errors.push(e)
    })
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
