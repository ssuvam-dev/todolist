<template>
    
    <td><input type="checkbox" id="checkbox" class="form-check-input" v-model="checked" /></td>
      <td>{{ task }}</td>
      <td v-if="checked"><h5 class="text-success">Completed</h5></td>
      <td v-else><h5 class="text-danger">Pending</h5></td>
      <td> <inputComponentVue field_type="button" class="btn btn-danger" value="Delete" @click="deleteTask(index)"></inputComponentVue> </td>
  


</template>

<script>
    
import inputComponentVue from './inputComponent.vue';
    export default{
        name:'task',
        props:{
             task:String,
             index:Number,
             tasks:Array,
            
        },
        components:{
            inputComponentVue,
        },
        data(){
            return{
                checked:false
            }
        },
        methods:{
            deleteTask(index){
                this.tasks.splice(index,1);
                

            }
        }
       
    }
</script>