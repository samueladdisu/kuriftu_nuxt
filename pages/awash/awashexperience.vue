<template>
  <div class="main">
   <Destinationheader :src="require(`../../assets/image/AWASH-Color side.svg`)" />
    <div class="destination-links">
      <div class="container">
        <div class="wrapper">
       <ul class="link-destination">
            <li>
              <nuxt-link  class="a-link active" to="/destinationawash">Awash</nuxt-link 
              ><img src="../../assets/image/Icons/next2.svg" alt="" />
            </li>
            <li><nuxt-link  class="a-link " to="awashaccommodation"> <p>Accomodation</p> </nuxt-link > </li>
          
            <li><nuxt-link  class="a-link  active"  to="awashexperience">Experiences   <hr class="activeline"></nuxt-link ></li>
            <li><nuxt-link  class="a-link "  to="awashwellness">Wellness</nuxt-link ></li>
            <li><nuxt-link  class="a-link "  to="awashdining">Dining</nuxt-link ></li>
            <li>
              <nuxt-link  class="a-link " to="awashevent">Celebration & Events</nuxt-link >
              </li>
                <li><nuxt-link  class="a-link "   to="awashgallery">Gallery</nuxt-link ></li>
            <li>
              <nuxt-link  class="a-link " to="https://versavvymedia.com/reservation_system/reserve.php">Reserve</nuxt-link >
              </li>
          </ul>
          <hr class="line" />
        </div>
      </div>
    </div>
    <section class="display-video">
      <div class="container">
        <div class="video-wrapper">
          <img src="../../assets/image/Awash-bg.jpg" alt="" />
        </div>
      </div>
    </section>
  
<section class="general-experience">
<div class="container">
  <div class="all-wrapper">
      <div class="see-more">
           <p>Experience</p>
          <hr class="see-line" />
       
        </div>
        <div class="all-cards">
          <div class="single-card" data-aos="fade-up"  data-aos-duration="3000">
            <img src="../../assets/image/crocodial.jpg" alt="">
            <h3>Crocodile Viewing</h3>
            <p>Kuriftu Awash is the perfect destination for people who want to pair their exhilarating adventures with creature comforts. On the banks of the river you can watch lazy crocodiles snoozing in the sun or floating in the river like dead logs of wood You can spend an enjoyable few hours marveling at their strong jaws, scaly backs and large nostrils lurking just beneath the water surface. </p>

          </div>
           <div class="single-card " data-aos="fade-up">
           
                    <img  class="right-card" src="../../assets/image/awash-room4.jpg" alt="">
           <h3>Birdwatching </h3>
            <p>Witness the so many truly amazing birds with exceptional appearances </p>

          </div>
            <div class="single-card" data-aos="fade-up"  data-aos-duration="3000">
            <img src="../../assets/image/awashfalls.jpg" alt="">
            <h3>Camel Riding</h3>
            <p>Head out into the sunset as part of a camel caravan as you take in the breath-taking beauty</p>

          </div>
            <div class="single-card " data-aos="fade-up">
           
                    <img  class="right-card" src="../../assets/image/awashfalls.jpg" alt="">
         
<h3>Safari Tours</h3>
            <p> If you are a nature lover and wish to experience some of the culture and history that surrounds us, then have a look at our safari tour. Awash has unique landscapes making ita wonder to experinace.</p>
          </div>
            
           
         
           
        </div>
        
  </div>
</div>
</section>
   
    
  
  </div>
</template>

<script>
import AOS from "aos";
import "aos/dist/aos.css";
import Event from "../../components/Event.vue";
export default {
  mounted() {
    AOS.init({
      duration: 1500,
      offset: 120,
      easing: "ease",
      once: false,
      anchorPlacement: "top-bottom",
    });
  },
};
</script>

<style lang="scss" scoped>
.main {
     header {
    width: 100%;
    height: 10vh;
    position: relative;

    &::after {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgb(0, 6, 27);
    }
    nav {
      z-index: 999;
      position: absolute;
      width: 100%;
      height: 100%;
      top: 0;
      left: 0;

      .top-nav {
        position: sticky;
        top: 0;
        bottom: 0;
        width: 90%;
        margin: 0 auto;
      }
      .container {
        display: flex;
        align-items: flex-start;
        justify-content: space-between;
        .menu-line {
          margin-top: 1rem;
          cursor: pointer;
          .line {
            hr {
              margin: auto;
              margin-top: 1rem;
              color: $kuriftu-black;
              // height: 10rem;
              width: 2.35rem;
            }
          }
        }
        .logo {
          margin-top: 1rem;
          width: 9rem;
          @include responsive($md) {
            width: 11rem;
          }
        }
        .nav-book-button {
          display: none;
        }
      }
    }
  }
  @include responsive($lg) {
    header {
      nav {
        .container {
          align-items: center;

          .nav-book-button {
            margin-top: 1rem;
            display: block;
            .wrapper {
              display: flex;
              gap: 1rem;
              .social {
                display: flex;
                gap: 0.5rem;
                .icon {
                  width: 1rem;
                }
              }
            }
          }
        }
      }
    }
  }
  .destination-links {
    display: none;
  }
  @include responsive($lg) {
    .destination-links {
      display: block;
      .container {
        .wrapper {
          .link-destination {
            display: flex;
            margin-top: 4rem;
            gap: 3rem;
            place-content: center;
            li {
              display: flex;
              align-items: center;
              .a-link {
                color: $kuriftu-grey;
                font-size: 0.88rem;
              }
              .active {
                color: $kuriftu-black;
                font-weight: 600;
              }
            }
            .activeline{
               margin-top: .6rem;
               margin-bottom: -1.1rem;
                  color: $kuriftu-black;
                      opacity: 1;
            }
          }
          .line {
            // border-style:solid ;
            color: $kuriftu-grey;
            @include  responsive($xl){
 width: 60rem;
            }
           
            margin-top: .6rem;
            opacity: 0.7;
          }
        }
      }
    }
  }
  .display-video {
    margin-top: 4rem;
  }
  @include responsive($md) {
    .display-video {
      margin-top: 5rem;
    }
  }
 .general-experience{
   margin-top: 5rem;
   @include responsive($md){
     margin-top: 8rem;
   }
   .container{
     .all-wrapper{
         .see-more {
        display: flex;
        align-items: center;
        gap: 2rem;
        margin-top: 3rem;
        @include responsive($md) {
          margin-top: 5rem;
        }
        hr {
          border-style: solid;
          color: $kuriftu-grey;
          opacity: 0.5;

          width: 100%;
        }
        p {
          font-size: 0.7rem;
          text-transform: uppercase;
          color: $kuriftu-grey;
          width: 6rem;
        }
      }
      .all-cards{
        @include responsive($md){
          display: grid;
          grid-template-columns: 1fr 1fr ;
          gap: 1rem;
        }
         @include responsive($lg){
        
          gap: 5rem;
        }
      
        .single-card{
          margin-top: 3rem;
        
            .right-card{
          margin-top: 6rem;
        }
          img{
            width: 20rem;
            height: 25rem;
            object-fit: cover;
             @include responsive($lg){
         width: 100%;
         height: 35rem;
        }
          }
          h3{
            @extend .title;
            font-size: 1rem;
            margin-top: .98rem;
            text-transform: uppercase;
          }
          p{
            @extend .text;
            margin-top: .98rem;
            width: 20rem;
              font-size: .95rem;
                 @include responsive($lg){
         width: 100%;
     
        }
          }
        }
      }
     }
   }
 }
}
</style>
