<template>
  <div id="app">
   <h2>Меню:</h2>
   <pizza v-bind:pizzaName='"Пицца от школы программистов"' v-bind:pizzaPrice='599'>
     <p>На самом деле не 599, а 600, но никто ведь не заметит отсутствие одного рубля со сдачи, верно?</p>
   </pizza>
   <pizza v-bind:pizzaName='"Пицца от 6Б"' v-bind:pizzaPrice='12'>
     <p>Потому и 12 рублей</p>
   </pizza>
   <pizza v-bind:pizzaName='"Мандарины"' v-bind:pizzaPrice='"некоторое количество"'>
     <p>ура новый год</p>
   </pizza>
  </div>
</template>

<script>
import Pizza from './components/Pizza.vue'

export default {
  name: 'app',
  data(){
    return {
      
    }
  },
  components: {
    pizza: Pizza
  } 
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>