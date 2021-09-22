<template>
  <div class="choose-comics">
    <div class="container-comics">
      <div id="current-series"><h3>CURRENT SERIES</h3></div>
      <div class="single-comic" v-for="(comic, index) in comics" :key="index">
        <img :src="comic.thumb" :alt="comic.series">
        <p>{{comic.series.toUpperCase()}}</p>
      </div>
      <div class="center">
        <button>LOAD MORE</button>
      </div>
    </div>
  </div>
</template>

<script>
import Links from "../assets/img/data/Links.js";
export default {
    name: "ChooseComics",
    
    data(){
      return{
        comics: Links
      }
    }
  }
</script>

<style scoped lang="scss">
@import "@/style/generals";
@import "@/style/mixins";
@import "@/style/vars";
.choose-comics{
  width: 100%;
  height: 600px;
  background-color: $secondary-color;
  position: relative;

  .container-comics{
    width: 1170px;
    height: 600px;
    margin: 0 auto;
    display: flex;
    flex-wrap: wrap;
    align-self: center;

    #current-series{
      padding: 10px 40px;
      background-color: $primary-color;
      position: absolute;
      top: -20px;

        h3{
          color: white;
        }
    }

    .single-comic{
      margin-top: 40px;
      flex-basis: calc(100% / 6);
      justify-content: center;
      cursor: pointer;

        img{
          height: 160px;
          width: 160px;
          object-position: top;
          object-fit: cover;
        }

        p{
          color: white;
          font-size: 10px;
          margin-top: 15px;
        }
    }
    .center{
      width: 100%;
      display: flex;
      justify-content: center;
      button{
        background-color: $primary-color;
        color: white;
        padding: 0 80px;
        margin: 30px 0 20px 0;
      }
    }
  }
}
</style>