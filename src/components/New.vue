<template>
    <div class="new">
        <h1>This is a new component</h1>
        <h2>created by {{ name }}</h2>
        <button v-on:click="hello">click here</button>
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
            name: 'sifat'
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
</style>