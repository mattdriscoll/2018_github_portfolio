<template>
  <div class="body-background">
    <app-nav></app-nav>
    <section class="container">
      <app-background></app-background>
      <app-avatar></app-avatar>
      <app-slider></app-slider>
    </section>
  </div>
</template>

<script>
import AppNav from '~/components/AppNav.vue'
import AppAvatar from '~/components/AppAvatar.vue'
import AppSlider from '~/components/AppSlider.vue'
import AppBackground from '~/components/AppBackground.vue'

export default {
  components: {
    AppNav,
    AppAvatar,
    AppSlider,
    AppBackground
  },
  methods: {
    fadeBackground: () => document.querySelector('.gradient-background').classList.add('animated'),
    fadeAvatar: () => document.querySelector('.avatar').classList.add('animated')
  },
  mounted () {
    setTimeout(this.fadeBackground, 400);
    setTimeout(this.fadeAvatar, 800);
  }
}
</script>
