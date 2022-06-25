<template>
  <div>
    <Header
      v-bind:image="image"
      title="Skills"
      icon="fa-solid fa-dumbbell"
      subtitle=""
    />
    <Section>
      <div class="grid grid-cols-2 md:grid-cols-4 gap-4 pt-4">
        <div v-for="skill in skills" :key="skill">
          <ul class="fa-ul">
            <li class="text-left">
              <span class="fa-li"><i class="fa-solid fa-check-square"></i></span
              >{{ skill }}
            </li>
          </ul>
        </div>
      </div>
    </Section>
  </div>
</template>
<script>
import img from 'assets/img/skills.webp'
export default {
  data () {
    return {
      image: img,
      skills: [
        'C/C++',
        'Java',
        'Python',
        'Android Studio',
        'JavaScript',
        'Vue.js',
        'Nuxt.js',
        'Laravel',
        'Node.js',
        'WebSockets',
        'MySQL',
        'MariaDB',
        'PHP',
        'WordPress',
        'Rest API',
        'Bootstrap',
        'TailwindCSS',
        'Jekyll',
        'Git',
        'Adobe Photoshop'
      ]
    }
  },
  head: {
    title: 'Skills - Prashant Upreti',
    meta: [
      {
        hid: 'description',
        name: 'description',
        content: 'Skills Page'
      }
    ]
  }
}
</script>
