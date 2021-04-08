<template>
  <div class="home">
    <div class="fish-icon">

    </div>
    <p>Your cat</p>
    <p>is</p>
    <p>Our cat</p>
    <img class="img-cat" alt="Vue logo" src="../assets/scottish-bg.png" />
    <p class="bg-text">CATS</p>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "Home",
  components: {

  }
};
</script>

<style scoped>
.img-cat{
  width: 1160px;
}
.home{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  position: relative;
}
.home p{
  margin: 0;
  font-weight: 900;
}
.home p:nth-child(2){
  font-size: 48px;
  letter-spacing: 5px;

}
.home p:nth-child(3){
  letter-spacing: 5px;

  font-size: 36px;
}
.home p:nth-child(4){
  letter-spacing: 5px;

  font-size: 68px;
  color: rgb(50,156,206);
}
.fish-icon{
  font-size: 32px;
  margin-bottom: 30px;
  color: #aeaeae;
}
.fish-icon svg{
  margin: 0px 25px;
}
.fish-icon svg:nth-child(1){
  transform: rotate(30deg);
}
.fish-icon svg:nth-child(2){
  transform: rotate(-30deg);
  margin-bottom: 15px;
}
.fish-icon svg:nth-child(3){
  transform: rotate(30deg);
}
.bg-text{
  letter-spacing: 80px;
  position: absolute;
  z-index: -1;
  font-size: 450px;
  top: 50px;
  background: -webkit-linear-gradient(#e6e6e6, #FFFF);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
</style>
