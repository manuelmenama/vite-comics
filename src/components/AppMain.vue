<script>
export default {
      name: 'AppMain'
}
</script>

<template>

  <main>

    <h1 class="container">Main</h1>

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