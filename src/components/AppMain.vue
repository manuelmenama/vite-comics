<script>
import AppCTAElement from './AppCTAElement.vue';

export default {
  name: 'AppMain',
  components: {
    AppCTAElement
  }
}
</script>

<template>

  <main>

    <div class="jumbotron">

      <img src="../assets/img/jumbotron.jpg" alt="">

    </div>

    <h1 class="container">Main</h1>

    
    <AppCTAElement />

  </main>
  
</template>

<style lang="scss" scoped>

@use '../style/partials/variables' as *;

main{
  background-color: $background-color;
  h1{
    padding: 40px 0;
    color: white;
  }
}

</style>