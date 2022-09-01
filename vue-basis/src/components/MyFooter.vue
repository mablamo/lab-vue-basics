<script setup>
import { ref } from 'vue';

const pressed = ref(false);
let lista = [
    {
        title: 'Lord of the rings',
        description: 'Very good film',
        content: 'three films'
        },
    {
        title: 'Zelda',
        description: 'Very good game',
        content: 'the best is OoT'
        },
    {
        title: 'Yiruma',
        description: 'Musician',
        content: 'several songs'
        },
]
</script>

<template>
    <h2>this is the footer</h2>
    <button @click="pressed = !pressed">Press Me!</button>
    <h3 v-if="pressed">Hello!</h3>
    <p v-for="item in lista">{{item.title}}</p>
</template>

<style>

h2{
    color: blue;
    background-color: yellow;
}

</style>
