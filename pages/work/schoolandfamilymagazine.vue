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
      title: 'School and Family Magazine',
      subtitle: 'Print magazine for school districts',
      imgsrc: 'work_schoolfamily.jpg',
      websiteFeatures: [
        'Custom Wordpress theme',
        'Joomag magazine viewing API',
        'Modular CSS (SASS)',
        'CMS-driven'
      ],
      siteHref: 'http://schoolandfamilymagazine.com'
    }
  },
  components: {
    ProjectDetails
  }
}
</script>
