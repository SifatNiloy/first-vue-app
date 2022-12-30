<template>
    <div>
        <h1>Hello from home component</h1>
        <h1>{{ data }}</h1>
        <h1>{{ msg }}</h1>
        <button v-on:mouseover="hello('data')">Call hello function</button>
        <h2 v-if="show">Conditional Rendering in vue js</h2>
        <h2 v-else>else side</h2>
        <button v-on:click="display">Toogle</button>
        <br> <br>
        <table border="2px">
            <tr>
                <td>id</td>
                <td> name</td>
                <td>&nbsp;&nbsp;&nbsp; email</td>
            </tr>
            <tr v-for="user in users" :key='user.id'>
                <td>{{user.id}}</td>
                <td>{{user.name}}</td>
                <td>{{user.email}}</td>
            </tr>
        </table>
        
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
    },
    data(){
        return{
            users:[
                {id:1, name: "Asif", email: 'asif@gmail.com'},
                {id:2, name: "Iqbal", email: 'Iqbal@gmail.com'},
                {id:3, name: "siam", email: 'siam@gmail.com'},
                {id:4, name: "sifat", email: 'sifat@gmail.com'}
            ]
        }
    }
}
</script>