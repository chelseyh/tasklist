<template>
  <div id="app">
    <Header theheading="Task List"/>
  <Tasks v-bind:tasklist=task></Tasks>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Tasks from './components/Tasks.vue'
import axios from 'axios'

export default {
  name: 'App',
  components: {
    Header,
    Tasks
  },
  data(){
    return{
      tasks:
      [
        {id:0, title:"Learn HTML", completed: true},
        {id:1, title:"Learn Javascript", completed: false},
        {id:2, title:"Learn JS Framework VUE", completed: false}
      ]
    }
  },
  mounted()
  {
    axios.get('https://jsonplaceholder.typicode.com/todos')
    .then( (response) =>
    {
      console.log(response.data)
      this.tasks = response.data
    })
  }
}
</script>

<style>
  * {
    margin: 0px;
    padding: 0px;
  }

</style>
