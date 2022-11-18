<template>
    <div class="container">
            <div class="d-flex">
                <input type="text" class="form-control" placeholder="Enter your task" v-model="taskname"/>
                <button @click="createTask" type="button" class="btn btn-primary">Add</button>
            </div>
    </div>
    <tasksVue :tasks=tasks></tasksVue>
</template>

<script >
    import tasksVue from './tasks.vue';
    export default{
        name:'formContainer',
        components:{
            tasksVue,
         
        },
        data(){
            return {
                taskname:null,
                tasks:[],
              
            }
        },
        methods:{
            createTask(){
                this.tasks.push(this.taskname)
                this.taskname="";
        
            }
        }

    }
</script>
<style>
    button{
        margin-left: 10px;
    }
</style>