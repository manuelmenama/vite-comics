<script>

import ctaIcon from '../data/cta-icon';

export default {
  name: 'AppCTAElement',
  data() {
    return {
      ctaIcon
    }
  },
  methods: {
    getImagePath: function(imgPath) {
      return new URL(`../assets/img/${imgPath}`, import.meta.url).href;
    }
  }
}
</script>

<template>

  <div class="cta-bar">
    <div class="container col">
      
      <ul>
  
        <li
          v-for="(icon, index) in ctaIcon"
        :key="index">
          <img :src="getImagePath(icon.image)" alt="">
          <a href="#">{{icon.text}}</a>
        </li>
  
      </ul>
    </div>



  </div>
  
</template>

<style lang="scss" scoped>

@use '../style/partials/variables' as *;
@use '../style/partials/mixin' as *;
 
.cta-bar{

  height: 120px;
  background-color: $main-color;

  .col{
    height: 100%;
  }

  ul{
    height: 100%;
    @include flex('between');
    align-items: center;
    @include removeStyle();
    li{
      @include flex('only');
      align-items: center;
    }
    li a{
      @include removeADecoration();
      font-size: 0.8rem;
      margin-left: 1rem;
      color: $text-color;
    }
  }

  img{
    width: 45px;
  }

}

</style>