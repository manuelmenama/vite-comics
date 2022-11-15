<script>
export default {
      name: 'AppHeader'
}
</script>

<template>

  <header>

    <div class="col container">

      <div class="logo">
        <img src="/dc-logo.png" alt="logo dc comics">
      </div>

      <nav>
        <ul>
          <li><a href="#">CHARACTERS</a></li>
          <li><a href="#">COMICS</a></li>
          <li><a href="#">MOVIES</a></li>
          <li><a href="#">TV</a></li>
          <li><a href="#">GAMES</a></li>
          <li><a href="#">COLLECTIBLES</a></li>
          <li><a href="#">VIDEOS</a></li>
          <li><a href="#">FANS</a></li>
          <li><a href="#">NEWS</a></li>
          <li><a href="#">SHOP</a></li>
        </ul>
      </nav>

    </div>

  </header>
  
</template>

<style lang="scss" scoped>

@use '../style/partials/variables' as *;
@use '../style/partials/mixin' as *;

header{
  background-color: $header-color;
  height: 100px;
  .col{
    @include flex('only');
    .logo img{
      width: 80px;
    }
    nav{
      font-size: 0.9rem;
      font-weight: 600;
      ul{
        @include removeStyle();
        @include flex('only');
        li a{
          @include removeADecoration();
        }
      }
    }
  }
}

</style>