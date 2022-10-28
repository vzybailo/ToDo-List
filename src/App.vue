<template>
  <div id="app">
    <h2>{{title}}</h2>
    <ListTask 
      :msg="msg"
      @removeTitle="removeTitle"/> 
  </div>
</template>

<script>
import ListTask from '@/components/ListTask.vue'

export default {
  components: {
    ListTask
  },
  data() {
    return {
      title: 'ToDO List',
      todolist: [

      ]
    }
  },
   methods: {
    changeTitle() {
      this.title = this.newTitle
      this.newTitle = ''
    },
     removeTitle(){
      this.msg = ''
      console.log('work')
    }
  },
}
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
