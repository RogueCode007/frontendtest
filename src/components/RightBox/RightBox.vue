<template>
  <div class="rightbox">
    <Circles />
    <transition-group
      :name="transition"
      tag="div"
      class="slider-wrapper"
    >
      <div
        v-for="number in [currentImg]"
        :key="number"
        class="slide slider-content"
      >
      <div class="inner">
        <div class="heroimg">
          <img :src="content[Math.abs(currentImg) % content.length].image" alt="">
        </div>
        <div class="card rounded p-2">
          <star-rating value="4" :disabled="true"></star-rating>
          <p class="text mt-2">{{ content[Math.abs(currentImg) % content.length].description }}</p>
          <div class="mt-4 flex items-end">
            <div class="avatar">
              <img :src="content[Math.abs(currentImg) % content.length].image2" alt="">
            </div>
            <div class="ml-3 word">
              <p class="font-bold name">{{ content[Math.abs(currentImg) % content.length].name }}</p>
              <p class="mt-1">{{ content[Math.abs(currentImg) % content.length].role }}</p>
            </div>
          </div>
        </div>
      </div>
      </div>
    </transition-group>
  </div>
</template>

<script>
import Circles from "../Circles.vue"
import image from "@/assets/hero.png"
import image2 from "@/assets/Ellipse 1.png"
import StarRating from './StarRating.vue'
export default {
  components:{
    Circles, StarRating
  },
  data() {
    return {
      show: true,
      transition: '',
      autoplay: null,
      content: [
        {
          name: 'Isaac Hayden',
          location: 'Lagos, Nigeria',
          description:
            'Great place to work with the good work culture and people skills.',
          role: "Business Analyst",
          image: image,
          image2: image2
        },
        {
          name: 'Obiwan Pelosi',
          location: 'Lagos, Nigeria',
          description:
            'I love this system, I will use this medium to learn and hire',
          role: 'HR Manager',
          image: image,
          image2: image2
        },
        {
          name: 'Dimitri Petrov',
          location: 'Lagos, Nigeria',
          description:
            'An amazing tool all round. excellent customer service',
            role: "Russian Spy",
          image: image,
          image2: image2
        },
        
      ],
      currentImg: 0
    }
  },
  mounted() {
    // this.playSlider()
  },
  beforeDestroy() {
    clearInterval(this.autoplay)
  },
  methods: {
    playSlider() {
      this.autoplay = setInterval(() => {
        this.currentImg = this.currentImg + 1
        this.transition = 'slide-right'
      }, 5000)
    },
    manualPlay() {
      clearInterval(this.autoplay)
      setTimeout(() => {
        this.playSlider()
      }, 1)
    },

  }
}
</script>

<style scoped lang="scss">
@import './styles';
@media only screen and (min-width: 1024px){
    .rightbox{
        // border: 1px solid red;
        width: 100%;
    }
    h1{
        font-size: 2em
    }
  .inner{
    height: 500px;
    width: 100%;
    
  // position: absolute;
  // bottom: 0;
  // left: 50%;
  // transform: translateX(-50%);
  }
//   .slider-wrapper{
//   border: 1px solid yellow;
//   width: 100%;
//   position: absolute;
//   bottom: 0;
//   left: 50%;
//   transform: translateX(-50%);
//   z-index: 10000;
// }
}
</style>