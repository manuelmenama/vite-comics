<script>
import AppCTAElement from './AppCTAElement.vue';
import AppCard from './AppCard.vue';
import dcComics from '../data/dc-comics'


export default {
  name: 'AppMain',
  components: {
    AppCTAElement,
    AppCard
  },
  data() {
    return {
      dcComics
    }
  }
}
</script>

<template>

  <main>

    <div class="jumbotron">

      <div class="button-fill">
        <p>CURRENT SERIES</p>
      </div>

    </div>

    <div class="container cont">
      
      <ul>

        <AppCard
          v-for="(card, index) in dcComics" 
          :key="index"
          :cardThumb="card.thumb"
          :cardSeries="card.series"/>

      </ul>

      <a
        class="button-fill a-btn"
        href="#">SHOW MORE</a>

    </div>

    
    <AppCTAElement />

  </main>
  
</template>

<style lang="scss" scoped>

@use '../style/partials/variables' as *;
@use '../style/partials/mixin' as *;

main{
  background-color: $background-color;
  width: 100%;
  .button-fill{
    @include button();
    position: absolute;
    bottom: -15px;
    left: 15%;
  }
  .button-fill.a-btn{
    bottom: 10px;
    left: 50%;
    transform: translateX(-50%);
    @include removeADecoration();
    color: $text-color;
  }
  .jumbotron{
    height: 250px;
    background-position: center top;
    background-size: cover;
    background-image: url("../assets/img/jumbotron.jpg");
    position: relative;
    
  }

  .cont{
    padding: 3rem 0;
    position: relative;
  }

  ul{
    width: 100%;
    @include removeStyle();
    @include flex('only');
    flex-wrap: wrap;
    text-align: center;
    
  }
}

</style>