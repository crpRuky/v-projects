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
  margin-top:0px;
  margin-bottom:10px;
  font-size:24px;
}
.info p {
  font-size:18px;
}

.main {
  padding:15px 0px 10px 0px;
  margin-top:20px;
  background-color:rgba(185, 185, 255, 0.25);
}
</style>
