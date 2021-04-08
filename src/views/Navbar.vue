<template>
  <div class="nav-bar">
    <div class="logo" @click="$router.push('/')">
      <p>Cats</p>
      <p>Shop</p>
    </div>
    <div class="nav-link">
      <p @click="$router.push('/')">Home</p>
      <p @click="$router.push('/about')">About us</p>
      <p @click="$router.push('/cat')">Breeds</p>
      <p @click="$router.push('/catfood')">Shop online</p>
    </div>

  </div>
</template>
<script>
export default {
  name:"Navbar"
}
</script>
<style scoped>
.nav-bar{
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.logo{
  display: flex;
  align-items: center;
  font-size: 42px;
  font-weight: 900;
}
.logo p:nth-child(1){
  color: rgb(50,153,206);
}
.logo p{
  margin: 0;
}
.nav-link{
  font-size: 20px;
  display: flex;
  align-items: center;
}
.nav-link p{
  margin: 0px 30px;
}
.bone-icon{
  color: #42b983;
}
</style>