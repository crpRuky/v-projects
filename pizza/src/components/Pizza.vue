<template>
    <div class="main">
        <h2>{{pizzaName}}</h2>
        <p>Цена: <b>{{pizzaPrice}}</b> белорусских рублей</p>

        <div class="info">
            <slot>
            </slot>
        </div>
    </div>
</template>

<script>
export default {
    props: ['pizzaName','pizzaPrice'],    
}
</script>

<style scoped>
h2 {
  margin-top:0px;
  margin-bottom:0px;
}
p {
  margin-top:5px;
  margin-bottom:10px;
  font-size:20px;
}
.info p {
  font-size:18px;
}

.main {
  position:relative;
  padding:15px 0px 10px 0px;
  box-shadow: inset 0px 2px 0px 0px #5a5a5a,
              0px -15px 20px -15px #a3a3a3;
  background-color:white;
  top:40px;
  margin-top:-40px;
  transition-duration:0.2s;
  transition-property:margin-top, top;
}
.main:hover {
  top:0px;
  margin-top:0px;
}
</style>
