<template>
    <div class="new">
        <h1>This is a new component</h1>
        <h2>created by {{ name }}</h2>
        <button v-on:click="hello">click here</button>
        <h2 v-bind:class="[checkDisplay?d:v]">Class with object</h2>
        <Users></Users>
        <Products></Products>
    </div>
</template>
<script>
import Users from './Users.vue';
import Products from './Products.vue';
export default {
    name: "Home",
    components: {
        Users,
        Products
    },
    data() {
        return {
            name: 'sifat',
            colorName:'skyblue',
            show:true,
            d:'display',
            v:'vueStyle',
            checkDisplay:true
        }
    },
    methods: {
        hello(){
            alert('Hello clicked')
        }
    }

}
</script>
<style>
.new {
    background-color: rgb(161, 208, 247);
    height: 800px;
    text-align: center;
}
.vueStyle{
    color: orange;
}
.display{
    background-color: rgb(131, 131, 250);
    padding: 5px;
}
</style>