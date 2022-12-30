<template>
    <div>
        <h1>form DataBind: {{message}}</h1>
        <input type="text" v-modal:value="message" >
    </div>
</template>
<script>
    export default{
        name:"DataBind",
        data(){
            return{
                message: 'Hi'
            }
        }
    }
</script>