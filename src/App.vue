<script>

    import headerFile from './components/header.vue'
    import formContainerVue from './components/formContainer.vue';
    import tasksVue from './components/tasks.vue';
   export default{
    name:'App',
    components:{
        headerFile,
        formContainerVue,
        tasksVue
    }
   }
</script>

<template>
 <headerFile></headerFile>
 <formContainerVue></formContainerVue>

</template>
