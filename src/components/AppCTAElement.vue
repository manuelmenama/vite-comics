<script>

import ctaIcon from '../data/cta-icon';

export default {
  name: 'AppCTAElement',
  data() {
    return {
      ctaIcon
    }
  }
}
</script>

<template>

  <div class="cta-bar">

    <ul>

      <li
        v-for="(icon, index) in ctaIcon"
      :key="index">
        <img :src="icon.image" alt="">
        <a href="#">{{icon.text}}</a>
      </li>

    </ul>


  </div>
  
</template>

<style lang="scss" scoped>

@use '../style/partials/variables' as *;

.cta-bar{

  height: 120px;
  background-color: $main-color;

}

</style>