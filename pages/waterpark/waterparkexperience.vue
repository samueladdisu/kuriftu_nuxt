<template>
  <div class="main">
   <Destinationheader :src="require(`../../assets/image/Icons/waterpark.svg`)"/>
    <div class="destination-links">
      <div class="container">
        <div class="wrapper">
       <ul class="link-destination">
            <li>
              <nuxt-link  class="a-link active" to="/destinationwaterpark">Water Park</nuxt-link 
              ><img src="../../assets/image/Icons/next2.svg" alt="" />
            </li>
         
       
            <li><nuxt-link  class="a-link  active"  to="waterparkexperience">Experiences   <hr class="activeline"></nuxt-link ></li>
          
            <li><nuxt-link  class="a-link "  to="waterparkdining">Dining</nuxt-link ></li>
            <li>
              <nuxt-link  class="a-link " to="waterparkevent">Celebration & Events</nuxt-link >
              </li>
                   <li><nuxt-link  class="a-link "   to="waterparkgallery">Gallery</nuxt-link ></li>
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
          <img src="../../assets/image/water-cover.jpg" alt="" />
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
            <img src="../../assets/image/waterpark2.jpg" alt="">
            <h3>Boomerang Pool</h3>
            <p>Whatever thrills you seek, you’ll find all sorts of ways to fill your day and the the boomrang slide is the perfect way  to let loose and laugh. </p>

          </div>
            <div class="single-card " data-aos="fade-up"  data-aos-duration="3000">
     <img  class="right-card" src="../../assets/image/kuriftu dec 22-5391-min (1).jpg" alt="">
            <h3>Triple Spiral Ride</h3>
            <p>Riders slide via hovering dips and twists into the oscillating funnels; this trip changes pace enough to maintain riders guessing what is round the following bend.</p>
            <!-- <img  class="right-card" src="../../assets/image/cycling.jpg" alt="">
            <h3>Cycling</h3>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae dolorem corrupti eos officiis est similique, quas sunt a ipsum explicabo libero aliquam sint inventore, temporibus vel. Delectus maxime magnam vitae. </p> -->

          </div>
            <div class="single-card" data-aos="fade-up"  data-aos-duration="3000">
            <img src="../../assets/image/kuriftu dec 22-5422-min (1).jpg" alt="">
            <h3>Kiddie Water House </h3>
            <p>Hang on tight! Family fun is what we’re all about and the small is stirring for the little kids. 
 </p>

          </div>
            <div class="single-card " data-aos="fade-up">
           
                    <img  class="right-card" src="../../assets/image/water-cover.jpg" alt="">
            <h3>Wave Pool </h3>
            <p>Splash your way through a thriling experience Moving to and fro  .Relax in the shallow area or grab a tube and hit the deeper end to ride the tides. </p>

          </div>
            <div class="single-card"  data-aos="fade-up"  data-aos-duration="3000">
            <img src="../../assets/image/kuriftu dec 22-5422-min (1).jpg" alt="">
            <h3>Fekat Circus </h3>
            <p>Join fekat circus for a fascinating experience </p>

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
            color: $kuriftu-blue;
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
