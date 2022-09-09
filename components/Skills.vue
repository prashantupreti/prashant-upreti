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
        'C/C++ (Proficient)',
        'Java (Proficient)',
        'Python (Proficient)',
        'Android Studio (Proficient)',
        'JavaScript (Proficient)',
        'Vue.js (Proficient)',        
        'React.js (Proficient)',        
        'Angular.js (Proficient)',        
        'Laravel (Proficient)',
        'Node.js (Proficient)',
        'WebSockets (Proficient)',
        'MySQL (Proficient)',
        'MariaDB (Proficient)',
        'PHP (Proficient)',
        'WordPress (Proficient)',
        'Rest API (Proficient)',
        'Bootstrap (Proficient)',
        'TailwindCSS (Proficient)',        
        'Git (Proficient)',
        'Adobe Photoshop (Proficient)'
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
