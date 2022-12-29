<template>
    <div>
        <h1>Hello from home component</h1>
        <h1>{{ data }}</h1>
        <h1>{{ msg }}</h1>
        <button v-on:mouseover="hello('data')">Call hello function</button>
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
    }
}
</script>