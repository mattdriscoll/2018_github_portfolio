<template>
  <div class="body-background">
      <app-nav></app-nav>
    <section class="container">
      <div class="project-page" :class="pageClass">
        <app-background></app-background>
        <nuxt-child></nuxt-child>
      </div>
    </section>
  </div>
</template>

<script type="text/javascript">
  import AppNav from '@/components/AppNav.vue'
  import AppBackground from '@/components/AppBackground.vue'
  export default {
    components: {
      AppNav,
      AppBackground
    },
    data () {
      return {
        pageClass: 'project-page--' + this.$route.name
      }
    },
    methods: {
      fadeBackground: function() {
        document.querySelector('.gradient-background').classList.add('animated')
      }
    },
    mounted () {
      setTimeout(this.fadeBackground, 400);
    }
  }
</script>
