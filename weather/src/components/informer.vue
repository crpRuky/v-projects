<template>
  <div class="app">
    <div class="informer-container">

      <div class="temperature">
        <img src="img/thermometer.png">
        <div class="temp-real">1</div>
        <div class="temp-feel">-3.8</div>
      </div>

      <div class="flex-break"></div>

      <div class="humidity">
        <img src="img/humidity.png"> 12 <small>%</small>
      </div>

      <div class="vertical-divider"></div>

      <div class="wind">
        <img src="img/wind.png"> 12 <small>м/с</small>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'informer',
  props: {
    
  }
}
</script>

<style>
.informer-container {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  flex-wrap: wrap;
  width: 400px;
  min-height: 255px;
  padding: 30px;
  background-image: url('../assets/forest.png');
  background-size: cover;
  background-position: center center;
  border-radius: 20px;
  box-shadow: 0px 0px 10px 0px rgba(50, 50, 50, 0.75);
}
</style>
