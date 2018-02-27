<template>
  <div class="slider">
    <div class="headers">
      <h1>Matt Driscoll</h1>
      <h2>Web Developer</h2>
    </div>
    <div class="slides">
      <p v-if="currentSlide==0">Hi, I'm Matt.  I'm a freelance web developer from Texas, currently living in DFW.  I enjoy building websites that stand out from the rest.  From small business sites to large scale web apps, I will help you develop a web presence that is sure to catch eyes and generate revenue.  Boo-ya.</p>
      <p v-if="currentSlide==1">Former Front End Web Developer at The Fowler Group where I built custom CMS-driven websites such as <nuxt-link to="/work/trinityyoga">Trinity Yoga</nuxt-link> and <nuxt-link to="/work/schoolandfamilymagazine">School and Family Magazine</nuxt-link>, static sites such as <nuxt-link to="/work/foxypropaganda">Foxy Propaganda</nuxt-link> and <nuxt-link to="/work/millerglassworks">Miller Glassworks</nuxt-link>, and custom Ruby on Rails apps.</p>
      <p v-if="currentSlide==2">My diverse set of skills include HTML, CSS, Javascript, PHP, Ruby, Adobe Photoshop and Illustrator, yada yada.  I primarily work in Node.js, but other stacks are no problem.</p>
    </div>
    <div class="slider-buttons">
      <i @click="prevSlide" class="fas fa-chevron-circle-left"></i>
      <i @click="nextSlide" class="fas fa-chevron-circle-right"></i>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      currentSlide: 0,
      slideCount: 3
    }
  },
  methods: {
    prevSlide () {
      if ( this.currentSlide <= 0 ) {
        this.currentSlide = this.slideCount - 1
      } else {
        this.currentSlide -= 1
      }
    },
    nextSlide () {
      if ( this.currentSlide >= this.slideCount - 1 ) {
        this.currentSlide = 0;
      } else {
        this.currentSlide += 1
      }
    }
  }
}
</script>
