<template>
  <div>
    <Header
      v-bind:image="image"
      title="Prashant Upreti"
      icon=""
      subtitle="A Computer Engineer in the making..."
    />
  </div>
</template>
<script>
import img from 'assets/img/bg.webp'
import Section from './Section.vue'
export default {
  data () {
    return {
      image: img
    }
  },
  components: { Section }
}
</script>
