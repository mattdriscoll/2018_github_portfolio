<template lang="html">
  <div class="work-index">
    <div class="page-content">
      <h1>Portfolio</h1>
      <div class="project-links">
        <div v-for="project in projects" class="project-link">
          <nuxt-link :to="project.link">
            <img :src="project.imgSrc" :alt="project.title">
            <p>{{ project.title}}</p>
          </nuxt-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      projects: [
        {
          title: 'Trinity Yoga',
          link: '/work/trinityyoga',
          imgSrc: '/img/work_sm_trinity.jpg'
        }, {
          title: 'School And Family Magazine',
          link: '/work/schoolandfamilymagazine',
          imgSrc: '/img/work_sm_schoolfamily.jpg'
        }, {
          title: 'Foxy Propaganda',
          link: '/work/foxypropaganda',
          imgSrc: '/img/work_sm_foxy.jpg'
        }, {
          title: 'Miller Glassworks',
          link: '/work/millerglassworks',
          imgSrc: '/img/work_sm_miller.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="css">
</style>
