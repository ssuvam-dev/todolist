<template>
     <input :type='field_type' class="form-control" :class="class_name" :placeholder="placeholder_name" :value="value"/>
</template>
<script>
    export default{
        name:'inputComponent',
        props:{
            placeholder_name:{
                type: String,
                required:false,
            },
            field_type:{
                type:String,
                required:true
            },
            class_name:{
                type:String,
                required:false
            },
            value:{
                type:String,
                required:false
            },
        }   
    }
</script>