<template>
  <div class="slide-bar" v-bind:style="{ left: curPage + 'px' }">
    <div class="slides">
      <input type="radio" class="radio-btn" id="radio-1">
      <input type="radio" class="radio-btn" id="radio-2">
      <input type="radio" class="radio-btn" id="radio-3">
      <input type="radio" class="radio-btn" id="radio-4">
      <input type="radio" class="radio-btn" id="radio-5">
      <!--      <div class="prev-tab">-->
      <label class="prev-test" @click="togglePrev()">
        <font-awesome-icon icon="chevron-left" />
      </label>
      <!--      </div>-->
      <div class="card-slide slide" v-bind:class="['slide-'+curPage]">
        <div class="know-butt">
          <p>
            Know more
          </p>
          <font-awesome-icon icon="chevron-right"/>
        </div>
        <img class="card-img" alt="Vue logo" src="../assets/cat-card-1.png"/>
        <div class="card-desc">
          <div class="name-cat">
            <p>Scottish</p>
            <p>fold</p>
          </div>
          <p>dsadsaeqwesadasfaf
            wetewtwetdsfds</p>
        </div>
      </div>
      <div class="card-slide">
        <div class="know-butt">
          <p>
            Know more
          </p>
          <font-awesome-icon icon="chevron-right"/>
        </div>
        <img class="card-img" alt="Vue logo" src="../assets/cat-card-1.png"/>
        <div class="card-desc">
          <div class="name-cat">
            <p>Scottish</p>
            <p>fold</p>
          </div>
          <p>dsadsaeqwesadasfaf
            wetewtwetdsfds</p>
        </div>
      </div>
      <div class="card-slide">
        <div class="know-butt">
          <p>
            Know more
          </p>
          <font-awesome-icon icon="chevron-right"/>
        </div>
        <img class="card-img" alt="Vue logo" src="../assets/cat-card-1.png"/>
        <div class="card-desc">
          <div class="name-cat">
            <p>Scottish</p>
            <p>fold</p>
          </div>
          <p>dsadsaeqwesadasfaf
            wetewtwetdsfds</p>
        </div>
      </div>
      <div class="card-slide">
        <div class="know-butt">
          <p>
            Know more
          </p>
          <font-awesome-icon icon="chevron-right"/>
        </div>
        <img class="card-img" alt="Vue logo" src="../assets/cat-card-1.png"/>
        <div class="card-desc">
          <div class="name-cat">
            <p>Scottish</p>
            <p>fold</p>
          </div>
          <p>dsadsaeqwesadasfaf
            wetewtwetdsfds</p>
        </div>
      </div>
      <div class="card-slide">
        <div class="know-butt">
          <p>
            Know more
          </p>
          <font-awesome-icon icon="chevron-right"/>
        </div>
        <img class="card-img" alt="Vue logo" src="../assets/cat-card-1.png"/>
        <div class="card-desc">
          <div class="name-cat">
            <p>Scottish</p>
            <p>fold</p>
          </div>
          <p>dsadsaeqwesadasfaf
            wetewtwetdsfds</p>
        </div>
      </div>
      <label class="next-test" @click="toggleNext()">
        <font-awesome-icon icon="chevron-right"/>
      </label>
    </div>
  </div>
</template>
<script>
import axios from 'axios'
export default {
  name: "BreedCardSlider",
  data: function () {
    return {
      curPage: 200,
      cat_breeds_data:null
    }
  },
  mounted () {
    axios
        .get('https://api.thecatapi.com/v1/breeds?limit=5&page=0')
        .then(response => (this.cat_breeds_data = response.data))
  },
  methods: {
    toggleNext: function () {
      if (this.curPage < -80) {
        this.curPage = -200
      } else {
        this.curPage -= 200
      }
      console.log(this.cat_breeds_data)

    },
    togglePrev: function () {
      if (this.curPage > 0) {
        this.curPage = 200
      } else {
        this.curPage += 200
      }
      console.log(this.curPage)
    }
  }
}
</script>
<style scoped>
.next-test {
  font-size: 32px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: white;
  height: 50px;
  width: 50px;
  position: fixed;
  right: 0;
}

.prev-test {
  font-size: 32px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: white;
  height: 50px;
  width: 50px;
  position: fixed;
  left: 0;
  z-index: 99;
}

.know-butt {
  right: 0;
  top: 0;
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
  padding-right: 10px;
  font-size: 14px;
  font-weight: 500;
  color: white;
}

.slide-bar {
  width: 100vw;
  display: flex;
  position: relative;
  justify-content: center;
  align-items: center;
  transition: 1s;
}

.slides {
  display: flex;
  align-items: center;
  justify-content: center;
  position: fixed;
  bottom: 0;
}

input[type="radio"] {
  display: none;
}

.card-slide {
  display: flex;
  padding: 100px 10px 10px 10px;
  margin: 30px 10px;
  width: 280px;
  border-radius: 10px;
  background: linear-gradient(129deg, rgb(121, 178, 208) 0%, rgb(43, 137, 188) 100%);
  position: relative;
  transition: 1s;
}
.card-slide:hover{
  transform: scale(1.1);
}
.card-slide > p {
  position: absolute;
  font-size: 12px;
  font-weight: 500;
  color: whitesmoke;
  right: 10px;
  top: 0;
  display: flex;
  align-items: center
}

.card-img {
  width: 300px;
  height: 300px;
  position: absolute;
  left: -20px;
  top: -120px;
}

.card-desc {
  display: flex;
  flex-direction: column;
  margin-top: 100px;
}

.card-desc > p {
  display: flex;
  justify-content: center;
  align-items: center;
  letter-spacing: 1px;
  font-size: 14px;
}

.card-desc .name-cat p {
  font-size: 42px;
  font-weight: 700;
  margin: 0;
  color: white;
  letter-spacing: 2px;
}

#radio-1:checked ~ .first {
  margin-left: -40%;
  transition: 1s;
}

#radio-2:checked ~ .first {
  margin-left: -80%;
  transition: 1s;
}

#radio-4:checked ~ .first {
  margin-left: -20%;
  transition: 1s;
}
</style>