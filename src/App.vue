<template>
  <div>
    <!-- {{testing}} {{testing.length}} -->
    <!-- <Button/> -->
    <Todo/>
  </div>
</template>

<script>

// import Button from "./components/button.vue"
import Todo from './components/todo.vue'
export default {
  name: 'App',
  components: {
    // Button,
    Todo,
  },
  data(){
    return {
      testing: "Hello World"
    }
  }
  }
</script>

<style>
body{
  height: 100vh;
  display: grid;
  place-items: center;
  background-color: #2c2c2c;
  color: #fff;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fff;
  margin-top: 60px;
}
</style>