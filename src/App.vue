<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->

  <!-- normal way of passing data -->
  <apple vertu='I am apple' />
  <apple content='I am apple content' />

  <!-- passsing section through slots (default slot) -->
  <apple>
    <h2>I am slots</h2>
  </apple>

  <!-- passsing section through named slots - "header" -->
  <apple>
    <header>I am named slots </header>
  </apple>

  <!-- or -->
  <apple>
    <template v-slot:header>
      <h1>I am named slots using vslot</h1>
      </template>
  </apple>

  <!-- for slot with no name is called as default slot -  '<slot></slot>' in child component  -->
<apple>
    <template v-slot:default>
<h1>I am named slots using default</h1>
      </template>
  </apple>

<!-- for conditional based slot assignment we use slot props like below -->
<orange>
    <template v-slot:default="slotProps">
      {{slotProps.fruitName}}
      </template>
  </orange>
  <orange>
    <template v-slot:default="slotProps">
      {{slotProps.fruitName}} - {{slotProps.fruitColor}}
      </template>
  </orange>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

import apple from './components/apple.vue'

import orange from './components/orange.vue'

export default {
  name: 'App',
  components: {
    apple,orange
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: black;
  margin-top: 60px;
}
</style>
