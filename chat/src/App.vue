<template>
  <div id="app">
    <container></container>
    <chat-message>Hello World</chat-message>
  </div>
</template>

<script>
import container from './components/Container.vue'
import chatMessage from './components/ChatMessage.vue'

export default {
  name: 'App',
  components: {
    container,
    chatMessage
  },
  data(){
    return {
      
    }
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
