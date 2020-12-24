<template>
  <div id="app">
<UserCard nickname="romashka" first_name="Иван" second_name="Иванов" last_name="Иванович" adress="ул. Да да" email="somebody@email.com" phone="+7 (123) 456 78 90"/>
  </div>
</template>

<script>
import UserCard from './components/UserCard'

export default {
  name: 'App',
  components: {
    UserCard
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
