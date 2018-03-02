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
      title: 'Miller Glassworks',
      subtitle: 'Custom Architectual Glass',
      imgsrc: 'work_miller.jpg',
      websiteFeatures: [
        'Static-generated',
        'CSS animations',
        'Blazing fast SSR',
        'Modular CSS (SASS)'
      ],
      siteHref: 'http://schoolandfamilymagazine.com'
    }
  },
  components: {
    ProjectDetails
  }
}
</script>
