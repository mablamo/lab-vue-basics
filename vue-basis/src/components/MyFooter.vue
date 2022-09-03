<script setup>
import { ref } from 'vue';

const pressed = ref(false);
const backcolor = ref('none');
const lista = [
  {
    title: 'Lord of the rings',
    description: 'Very good film',
    content: 'three films',
  },
  {
    title: 'Zelda',
    description: 'Very good game',
    content: 'the best is OoT',
  },
  {
    title: 'Yiruma',
    description: 'Musician',
    content: 'several songs',
  },
];
function print() {
  console.log(backcolor);
}
</script>

<template>
    <h2>this is the footer</h2>
    <button @click="pressed = !pressed; backcolor = 'red'; print()">Press Me!</button>
    <h3 v-if="pressed">Hello!</h3>
    <p :class= backcolor
      v-for='item in lista' :key="item.id">{{item.title}} {{item.description}}</p>
</template>

<style>

h2{
    color: blue;
    background-color: yellow;
}

.red{
  background-color: red;
}

</style>
