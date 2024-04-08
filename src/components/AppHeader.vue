<script>
export default {
  name: "AppHeader",
}

</script>

<template>
  <div class="item_1">
    <div class="container">
      News
    </div>
  </div>
  <div class="item_2">
    <div class="container">
      Logo
    </div>
  </div>
  <div class="item_3">
    <div class="container">
      NavBar
    </div>
  </div>


</template>

<style scoped>
.container {
  width: 80%;
  max-width: 1200px;
  margin: auto;
  border: 2px dotted black;
  height: 100%;
}

.item_1 , .item_3{
  background-color: red;
  color: white;
  width: 100%;
  height: 50px;
}

.item_2{
  background-color: aqua;
  width: 100%;
  height: 100px;
}

</style>