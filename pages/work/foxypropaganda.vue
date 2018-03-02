<template>
  <div class="page-content">
    <project-details
      :title="title"
      :subtitle="subtitle"
      :img="imgsrc"
      :features="websiteFeatures"
      :siteHref="siteHref" >
    </project-details>
  </div>
</template>

<script>
import ProjectDetails from '@/components/WorkDescription.vue'

export default {
  data () {
    return {
      title: 'Foxy Propaganda',
      subtitle: 'Digital and Variable Printing',
      imgsrc: 'work_foxy.jpg',
      websiteFeatures: [
        'Static-generated',
        'Video background',
        'Blazing fast SSR',
        'Modular CSS (SASS)'
      ],
      siteHref: 'http://www.foxypropaganda.com'
    }
  },
  components: {
    ProjectDetails
  }
}
</script>
