<template>
  <div>
    <Header
      v-bind:image="image"
      title="About Me"
      icon="fa-solid fa-person-circle-question"
      subtitle=""
    />
    <Section
      ><p class="text-lg leading-relaxed">
        ...
      </p></Section
    >
  </div>
</template>
<script>
import img from 'assets/img/about.webp'
export default {
  data () {
    return {
      image: img
    }
  },
  head: {
    title: 'About - Prashant Upreti',
    meta: [
      {
        hid: 'description',
        name: 'description',
        content: 'About Page'
      }
    ]
  }
}
</script>
