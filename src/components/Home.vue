<template>
    <div>
        <h1>Hello from home component</h1>
        <h1>{{ data }}</h1>
        <h1>{{ msg }}</h1>
        <button v-on:mouseover="hello('data')">Call hello function</button>
        <h2 v-if="show">Conditional Rendering in vue js</h2>
        <h2 v-else>else side</h2>
        <button v-on:click="display">toogle</button>
    </div>
</template>
<script>
export default{
    name: 'Home',
    props:{
        data: String,
        msg: String
    },
    methods:{
        hello(item)
        {
            alert(item)
        }
    },
    data(){
        return{
            show: false
        }
    },
    methods:{
        display()
        {
            this.show= !this.show
        }
    }
}
</script>