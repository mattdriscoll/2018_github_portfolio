<template>
  <div class="slider">
    <div class="headers">
      <h1>Matt Driscoll</h1>
      <h2>Web Developer</h2>
    </div>
    <div class="slides">
      <p v-show="currentSlide==0">
        Hi, I'm Matt.  I'm a freelance web developer from Texas, currently living in DFW.  I enjoy building websites that stand out from the rest.  From small business sites to large scale web apps, I will help you develop a web presence that is sure to catch eyes, look great on any screen, and generate revenue.
      </p>
      <p v-show="currentSlide==1">
        Web Developer at <a href="http://www.thestarrconspiracy.com" target="_blank">The Starr Conspiracy</a>.  I build full-scale web apps, custom CMS-driven websites, e-commerce sites, static-generated sites, and email campaigns.  See some examples of my <nuxt-link to="/work">work.</nuxt-link>
      </p>
      <p v-show="currentSlide==2">
        My diverse set of skills include HTML, CSS, Javascript, PHP, Ruby, Jekyll, Vue, Nuxt, Wordpress, Adobe Photoshop and Illustrator.  I primarily work in Node.js, but other stacks are no problem.
      </p>
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
