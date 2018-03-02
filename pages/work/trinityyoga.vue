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
      title: 'Trinity Yoga',
      subtitle: 'Small town yoga studio',
      imgsrc: 'work_trinity.jpg',
      websiteFeatures: [
        'Custom Wordpress theme',
        'MindBody scheduling API',
        'Modular CSS (SASS)',
        'CMS-driven'
      ],
      siteHref: 'http://www.trinityyogatx.com'
    }
  },
  components: {
    ProjectDetails
  }
}
</script>
