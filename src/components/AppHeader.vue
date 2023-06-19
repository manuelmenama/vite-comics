<script>
export default {
      name: 'AppHeader',
      data() {
        return {
          headerLink: [
            {
              text: 'CHARACTERS',
              link: '#',
              current: false
            },
            {
              text: 'COMICS',
              link: '#',
              current: false
            },
            {
              text: 'MOVIES',
              link: '#',
              current: true
            },
            {
              text: 'TV',
              link: '#',
              current: false
            },
            {
              text: 'GAMES',
              link: '#',
              current: false
            },
            {
              text: 'COLLECTIBLES',
              link: '#',
              current: false
            },
            {
              text: 'VIDEOS',
              link: '#',
              current: false
            },
            {
              text: 'FANS',
              link: '#',
              current: false
            },
            {
              text: 'NEWS',
              link: '#',
              current: false
            },
            {
              text: 'SHOP',
              link: '#',
              current: false
            }
          ]
        }
      }
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
          <li
            v-for="(link, index) in headerLink"
            :key="index">
            <a
              :class="{'active': link.current}"
              :href="link.link">{{link.text}}</a>
          </li>
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
  height: 130px;
  .col{
    height: 100%;
    @include flex('only');
    .logo{
      width: 30%;
      height: 100%;
      @include flex('start-center');
      img{
        height: 80px;
      }
    }
    nav{
      width: 70%;
      font-size: 0.9rem;
      font-weight: 600;
      ul{

        @include removeStyle();
        @include flex('between');
        line-height: 130px;
        li a{
          display: inline-block;
          height: 100%;
          &.active{
            color: $main-color;
            position: relative;
            &::after{
              content: '';
              display: inline-block;
              width: 100%;
              border-bottom: 5px solid $main-color;
              position: absolute;
              left: 0;
              bottom: 0;
              z-index: 999;
            }
          }
          @include removeADecoration();
        }
      }
    }
  }
}

</style>