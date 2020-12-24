<template>
  <div id="app">
    <UserCard v-bind:nickname="nickname" v-bind:image="image" v-bind:first_name="name.first" v-bind:second_name="name.second" v-bind:last_name="name.last" v-bind:adress="adress" v-bind:email="email" v-bind:phone="phone"/>
    <button v-on:click="getData()">Update</button>
  </div>
</template>

<script>
import UserCard from './components/UserCard'
import Image from './assets/70.jpg'

export default {
  name: 'App',
  components: {
    UserCard
  },
  data() {
    return {
      nickname: "romashka",
      image: Image,
      name: {
        first: "Иван",
        second: "",
        last: "Иванович",
      },
      adress: "ул. Пушкина",
      email: "somebody@email.com",
      phone: "+7 (123) 456-78-90"
    }
  },
  methods:{
    getData(){
      this.axios.get('http://37.77.104.246/users/getrandom.php')
      .then((response) => {
        this.name.first = response.data.firstName;
        this.name.last = response.data.lastName;
        this.image = response.data.img;
        this.adress = response.data.country + ", " + response.data.city + ", " + response.data.street;
        this.email = response.data.email;
        this.phone = response.data.phone;
        this.nickname = response.data.registered;
      })
    },
  },
  mounted(){
    this.getData();
  }
}
</script>

<style>
#app {
  display:flex;
  justify-content:center;
  flex-direction:column;
  align-items:center;
}
button {
  margin-top:20px;
  width:100px;
  height:40px;
  background-color: rgba(150, 174, 255, 0.178);
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  color: #2c3e50;
  font-weight:bold;
  font-size:18px;
  border:none;
  box-shadow: inset 0px -2px 0px 0px #8ba0ff, 
              inset 0px 2px 0px 0px #8ba0ff,
              inset 0px 0px 0px 0px #465ec9, 
              inset 0px 0px 0px 0px #465ec9;
  transition-duration:0.2s;
  transition-property:box-shadow, color;
  cursor:pointer;
  outline:none;
}
button:hover {
  box-shadow: inset 0px 0px 0px 0px #465ec9, 
              inset 0px 0px 0px 0px #465ec9,
              inset 0px -20px 0px 0px #8ba0ff, 
              inset 0px 20px 0px 0px #8ba0ff;
  color:#ffffff;
}
button:active {
  box-shadow: inset 0px -20px 0px 0px #465ec9, 
              inset 0px 20px 0px 0px #465ec9,
              inset 0px -20px 0px 0px #8ba0ff, 
              inset 0px 20px 0px 0px #8ba0ff;
  color:#ffffff;
  transition-duration:0.05s;
}
</style>
