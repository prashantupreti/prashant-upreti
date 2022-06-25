<template>
  <div>
    <Header
      v-bind:image="image"
      title="Education"
      icon="fa-solid fa-graduation-cap"
      subtitle=""
    />
    <Section class="text-center">
      <h2 class="mt-2 text-xl font-semibold md:text-4xl ">
        <i class="fas fa-certificate"></i> Bachelor of Science in Computer
        Engineering
      </h2>
      <h3 class="mt-2 text-lg md:text-2xl">
        Minor in Mathematics and Computer Science
      </h3>
      <h4 class="mt-2 text-md md:text-2xl font-semibold">
        <i class="fa-solid fa-building-columns"></i> Texas Tech University
      </h4>
      <p class="mt-2 text-md md:text-1xl">
        <i class="fa-solid fa-graduation-cap"></i> August 2022 &middot;
        <i class="fa-solid fa-trophy "></i> GPA: 3.5
      </p>
    </Section>
  </div>
</template>
<script>
import img from 'assets/img/education.webp'
import Section from './Section.vue'
export default {
  data () {
    return {
      image: img
    }
  },
  head: {
    title: 'Education - Prashant Upreti',
    meta: [
      {
        hid: 'description',
        name: 'description',
        content: 'Education Page'
      }
    ]
  },
  components: { Section }
}
</script>
