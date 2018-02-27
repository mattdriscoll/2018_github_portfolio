<template>
  <div class="body-background">
    <app-nav></app-nav>
    <section class="container">
      <div class="contact-page">
        <app-background></app-background>
        <div class="page-content">
          <h1>Contact</h1>
          <p>Have an idea for an awesome project?  Is your current site stuck on the 90s?  Get in touch!</p>
          <p><a :href="email" class="cta-link">Contact</a></p>
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
      // email: `mailto:%63%6F%6E%74%61%63%74%40%38%31%35%64%65%76%2E%63%6F%6D?subject=Let's%20Talk%20Websites!`
      email: `mailto:%6D%64%72%69%73%63%6F%6C%6C%38%31%35%40%67%6D%61%69%6C%2E%63%6F%6D?subject=Let's%20Talk%20Websites!`
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


URL-encoding : ASCII Character
%20 : space
%21 : !
%22 : ”
%23 : #
%24 : $
%25 : %
%26 : &
%27 : ‘
%28 : (
%29 : )
%2A : *
%2B : +
%2C : ,
%2D : –
%2E : .
%2F : /
%30 : 0
%31 : 1
%32 : 2
%33 : 3
%34 : 4
%35 : 5
%36 : 6
%37 : 7
%38 : 8
%39 : 9
%3A : :
%3B : ;
%3C : <
%3D : =
%3E : >
%3F : ?
%40 : @
%60 : `
%61 : a
%62 : b
%63 : c
%64 : d
%65 : e
%66 : f
%67 : g
%68 : h
%69 : i
%6A : j
%6B : k
%6C : l
%6D : m
%6E : n
%6F : o
%70 : p
%71 : q
%72 : r
%73 : s
%74 : t
%75 : u
%76 : v
%77 : w
%78 : x
%79 : y
%7A : z
