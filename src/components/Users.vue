<template>
    <div class="user">
        <h1>Users component</h1>
        {{ header }}
        <p v-html="header"></p>
        <p>{{ 1 + 100 }}</p>
        <h3>{{ ok ? "yes" : "no" }}</h3>
        <button v-bind:disabled="btnDisable" v-on:click="click">change value</button>
    </div>
</template>
<script>
export default {
    name: 'users',
    data() {
        return {
            ok: true,
            header:"<h1>template in vue js</h1>",
            btnDisable: true
        }
    },
    methods: {
        click() {
            this.ok= !this.ok
        }
    }
}
</script>
<style>
.user {
    height: 300px;
    width: 300px;
    background-color: rgb(210, 247, 168);
    padding: 20px;
}
</style>