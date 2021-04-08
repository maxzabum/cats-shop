<template>
  <div class="Cats">
    <div class="title">
      <h2>Our Bleeds</h2>
      <div class="main-title">
        <div class="left-title">
          <p>The world of cats</p>
        </div>
        <div class="right-title">
          <p>Discovery everything you need to know about cat. Take care with kindness and they will take care of you</p>
        </div>
      </div>
    </div>
    <BreedCardSilder/>
  </div>
</template>
<script>
import BreedCardSilder from "@/components/BreedCardSlider";

export default {
  components: {
    BreedCardSilder
  }
}
</script>
<style scoped>
.Cats {
  margin-top: 30px;
  height: 80vh;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.title {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 100px;
}

.title h2 {
  align-self: flex-start;
  color: rgb(43,141,193);
}


.main-title {
  display: flex;
  width: 450px;
}

.left-title {
  flex: 1;
  font-size: 32px;
  font-weight: 900;
}

.title p {
  margin: 0px;
}

.right-title {
  flex: 1;
  font-size: 16px;
}
</style>