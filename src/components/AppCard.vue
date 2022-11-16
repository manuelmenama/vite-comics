<script>
export default {
  name: 'AppCard',
  props: {
    cardThumb: String,
    cardSeries: String
  }
    
}
</script>

<template>

<li>
  <a href="#">
    <img :src="cardThumb" alt="">
    <p>
      {{cardSeries}}
    </p>
  </a>
</li>
  
</template>

<style lang="scss" scoped>

@use '../style/partials/variables' as *;
@use '../style/partials/mixin' as *;

li{
  width: calc(100% / 6);
  padding: 5px 5px;
  a{
    @include removeADecoration();
    color: $text-color;
    font-size: 0.7rem;
    img{
      width: 100%;
      height: 60%;
      object-fit: cover;
    }
  }
}
</style>