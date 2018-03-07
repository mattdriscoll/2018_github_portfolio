<template>
  <div class="body-background">
    <app-nav></app-nav>
    <section class="container">
      <div class="contact-page">
        <app-background></app-background>
        <div class="page-content">
          <h1>Contact</h1>
          <p>Have an idea for an awesome project?  Is your current site stuck on the 90s?  Interested in working together?  Get in touch!</p>
          <p><a :href="email.href" class="cta-link">{{ email.content }}</a></p>
        </div>
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
      email: {
        // href: `mailto:%6D%64%72%69%73%63%6F%6C%6C%38%31%35%40%67%6D%61%69%6C%2E%63%6F%6D?subject=Let's%20Talk%20Websites!`,
        href: `mailto:%6D%61%74%74%40%38%31%35%64%65%76%2E%63%6F%6D?subject=Let's%20Talk%20Websites!`,
        content: `Email`
      }
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
