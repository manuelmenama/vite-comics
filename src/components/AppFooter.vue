<script>
export default {
  name: 'AppFooter',
  data() {
    return {
      footerLinks: [
        
        {
          section: "DC COMICS",
          titles: [
            {
              title: "Characters",
              link: "#"
            },
            {
              title: "Comics",
              link: "#"
            },
            {
              title: "Movies",
              link: "#"
            },
            {
              title: "TV",
              link: "#"
            },
            {
              title: "Games",
              link: "#"
            },
            {
              title: "Videos",
              link: "#"
            },
            {
              title: "News",
              link: "#"
            }
          ]
        },
        {
          section: "SHOP",
          titles: [
            {
              title: "Shop DC",
              link: "#"
            },
            {
              title: "Shop DC Collectibles",
              link: "#"
            }
          ]
        },
        {
          section: "DC",
          titles: [
            {
              title: "Terms Of Use",
              link: "#"
            },
            {
              title: "Ad Choices",
              link: "#"
            },
            {
              title: "Advertisings",
              link: "#"
            },
            {
              title: "Jobs",
              link: "#"
            },
            {
              title: "Subscriptions",
              link: "#"
            },
            {
              title: "Talent Workshop",
              link: "#"
            },
            {
              title: "CSPC Certificate",
              link: "#"
            },
            {
              title: "Ratings",
              link: "#"
            },
            {
              title: "Shop Help",
              link: "#"
            },
            {
              title: "Contact Us",
              link: "#"
            }
          ]
        },
        {
          section: "SITES",
          titles: [
            {
              title: "DC",
              link: "#"
            },
            {
              title: "MAD Magazine",
              link: "#"
            },
            {
              title: "DC Kids",
              link: "#"
            },
            {
              title: "DC Power Visa",
              link: "#"
            }
          ]
        }
      ]
    }
  }
}
</script>

<template>

  <footer>

    <div class="upper-footer">
      <div class="col container">
        <div class="footer-link">
          <ul class="first-ul">
    
            <li
              class="first-li"
              v-for="(title, index) in footerLinks"
              :key="index">
    
              <h3>{{title.section}}</h3>
    
              <ul>

                <li
                  v-for="(link, index) in title.titles"
                  :key="index">
                  <a :href="link.link">{{link.title}}</a>
                </li>
                
              </ul>
    
            </li>
    
          </ul>
        </div>
        <div class="big-logo">        
          <img src="../assets/img/dc-logo-bg.png" alt="">
        </div>
      </div>

    </div>

    <div class="lower-footer container">

      <div class="button-container">

        <a href="#">SIGN-UP NOW!</a>

      </div>

      <div class="followus-container">

        <h2>FOLLOW US</h2>

        <img src="../assets/img/footer-facebook.png" alt="fb-logo">
        <img src="../assets/img/footer-twitter.png" alt="twitter-logo">
        <img src="../assets/img/footer-youtube.png" alt="yt-logo">
        <img src="../assets/img/footer-pinterest.png" alt="pintrest-logo">
        <img src="../assets/img/footer-periscope.png" alt="periscope-logo">

      </div>

  
    </div>

  </footer>
  
</template>

<style lang="scss" scoped>

@use '../style/partials/variables' as *;
@use '../style/partials/mixin' as *;

footer{
  background-color: $footer-color;
  height: 600px;
  width: 100%;
  .upper-footer{
    width: 100%;
    height: 100%;
    .col{
      @include flex('only');
    }
    .footer-link{
      width: 50%;
      height: 100%;
      ul.first-ul{
        height: 100%;
        width: 50%;
        h3{
          margin-bottom: 1rem;
          margin-top: 1rem;
        }
        @include removeStyle();

        li.first-li{
          margin: 1rem;
          display: flex;
          flex-direction: column;
          flex-wrap: wrap;
        }
        li.first-li a{
          @include removeADecoration();
          color: $footer-link-col;
          font-size: 0.8rem;
          margin-bottom: 0.2rem;
          
        }
      }
    }
    height: 70%;
    overflow: hidden;
    background-image: url(../assets/img/footer-bg.jpg);
    .big-logo{
      width: 50%;
      img{
        scale: 1.3;
        min-width: 500px;
      }
    }
  }
  .lower-footer{
    height: 30%;
    
    @include flex('between');
    align-items: center;

    .button-container a{
      display: inline-block;
      @include removeADecoration();
      color: $main-color;
      border: 2px solid $main-color;
      padding: 0.5rem 1rem;
    }
    .followus-container{
      
      @include flex('only');
      align-items: center;

      img{
        margin-left: 1rem;
      }
    }
  }
}

</style>