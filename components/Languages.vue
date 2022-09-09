<template>
  <div>
    <Header
      v-bind:image="image"
      title="Languages"
      icon="fa-solid fa-language"
      subtitle=""
    />
    <Section>
      <div class="grid md:grid-cols-3 gap-4 pt-4">
        <div v-for="language in languages" :key="language">
          <ul class="fa-ul">
            <li class="text-left text-xl">
              <span class="fa-li"><i class="fa-solid fa-language "></i></span
              >{{ language }}
            </li>
          </ul>
        </div>
      </div>
    </Section>
  </div>
</template>
<script>
import img from 'assets/img/languages.webp'
export default {
  data () {
    return {
      image: img,
      languages: ['English (Fluent)', 'Nepali (Native)', 'Hindi (Fluent)']
    }
  },
  head: {
    title: 'Languages - Prashant Upreti',
    meta: [
      {
        hid: 'description',
        name: 'description',
        content: 'Languages Page'
      }
    ]
  }
}
</script>
