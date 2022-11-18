<template>
  <table class="table table-striped">
  <thead>
    <tr>
    <th scope="col" width="10%">#</th>
      <th scope="col" width="50%">Task</th>
      <th scope="col" width="30%">Status</th>
      <th scope="col" width="10%">Delete</th>
    </tr>
  </thead>
  <tbody class="table-group-divider">
    <tr v-for="(task,index) of tasks" :key="index">
        <taskVue :task="task" :index=index :tasks="tasks"> </taskVue>
    </tr>
  </tbody>
</table>
</template>

<script>
import taskVue from './task.vue'
    export default{
        name:'tasks',
        components:{
            taskVue
        },
        props:{
            tasks:Array,
            index:String
        }
        }
       
    
</script>

<style scoped>
    table{
        margin-top: 20px;
        margin-left:10px;
    }
</style>