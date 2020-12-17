<template>
  <div id="app">
    <informer></informer>
  </div>
</template>

<script>
import informer from './components/informer.vue'


export default{
  components: { informer },
  name: 'MainApp',
  data(){
    return {text: 'Я новый компонент!'}
  }
}
</script>

<style>
  body {
    margin: 0px;
  }
</style>
