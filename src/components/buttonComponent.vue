<template>
    <button type="button" :class=" btn_class ">{{ btn_value }}</button>
</template>

<script>
    export default{
        name:'buttonComponent',
        props:{
            btn_class:String,
            btn_value:String
        }
    }
</script>

<style scoped>
    button{
        margin-left:10px;
    }
</style>