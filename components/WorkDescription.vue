<template>
  <div class="project-details">
    <div class="project-copy">
      <h1>{{ title }}</h1>
      <h3>{{ subtitle }}</h3>
    </div>
    <img :src="imgsrc" :alt="title">
    <div class="project-copy">
      <h2>Website Features:</h2>
      <ul>
        <li v-for="feature in features">{{feature}}</li>
      </ul>
      <a :href="siteHref" target="_blank" class="cta-link">View Site</a>
      <nuxt-link to="/work" class="cta-link">Back</nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  props: ['title', 'subtitle', 'img', 'features', 'siteHref'],
  computed: {
    imgsrc () {
      return `/img/${this.img}`
    }
  }
}
</script>
