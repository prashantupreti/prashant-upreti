<template>
  <div>
    <Header
      v-bind:image="image"
      title="Scholarships"
      icon="fa-solid fa-handshake-angle"
      subtitle=""
    />
    <Section>
      <div class="grid md:grid-cols-2 gap-4 pt-4">
        <div v-for="scholarship in scholarships" :key="scholarship">
          <ul class="fa-ul">
            <li class="text-left">
              <span class="fa-li"><i class="fa-solid fa-medal"></i></span
              >{{ scholarship }}
            </li>
          </ul>
        </div>
      </div>
    </Section>
  </div>
</template>
<script>
import img from 'assets/img/scholarships.webp'
export default {
  data () {
    return {
      image: img,
      scholarships: [
        'Presidential Scholarship, President’s List (Fall 2018, Spring 2019, Spring 2020)',
        'TTU Conoco CPCEED ENGR Scholarship (Spring 2019)',
        'TTU Study Abroad Desg Scholarship (Fall 2019)',
        'TTU Brewster FUSE End ENGR Scholarship (Fall 2020, Spring 2021)',
        'TTU DM Rich End ENGR Scholarship (Fall 2020, Spring 2021)',
        'TTU CV Bullen EE Scholarship (Fall 2021, Spring 2022)',
        'TTU Dawn Rich Quasi ENGR Scholarship (Fall 2021, Spring 2022)'
      ]
    }
  },
  head: {
    title: 'Scholarships - Prashant Upreti',
    meta: [
      {
        hid: 'description',
        name: 'description',
        content: 'Scholarships Page'
      }
    ]
  }
}
</script>
