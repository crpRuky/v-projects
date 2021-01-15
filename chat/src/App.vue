<template>
  <div id="app">
    <container>
      <chat-window v-on:sendData="sendMessage($event)">
        <chat-message v-for="(message, i) in messages" v-bind:key="i" :username="message.author" :datetime="message.datetime">{{message.text}}</chat-message>
      </chat-window>
    </container>
  </div>
</template>

<script>
import Container from './components/Container.vue'
import ChatMessage from './components/ChatMessage.vue'
import ChatWindow from './components/ChatWindow.vue'

export default {
  name: 'App',
  components: {
    Container,
    ChatMessage,
    ChatWindow
  },
  data(){
    return {
      messages:[]
    }
  },
  methods:{
    getMessages(){
      this.axios.get('http://37.77.104.246/api/chat/getmessages.php')
      .then((response) => {
        this.messages = response.data;
      })
    },
    sendMessage(data){
      let postBody = {
        author:data.author,
        text:data.text
      }
      let str = JSON.stringify(postBody);
      this.axios.post('http://37.77.104.246/api/chat/sendmessage.php', str)
      .then((response) => {
        console.log(response);
        this.getMessages();
      })
      .catch((error) => {
        console.log(error);
      });
    }
  },
  mounted(){
    this.getMessages();
  }
}
</script>

<style>
body {
  margin: 0;
  background-color: #f9f9fa;
}
</style>
