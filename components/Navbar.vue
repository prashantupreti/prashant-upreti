<script setup>
const colorMode = useColorMode()
console.log(colorMode.preference)
</script>
<template>
  <div>
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.1/css/all.min.css"
      integrity="sha512-KfkfwYDsLkIlwQp6LFnl8zNdLGxu9YAA1QvwINks4PhcElQSvqcyVLLD9aMhXd13uQjoXtEKNosOWaZqXgel0g=="
      crossorigin="anonymous"
      referrerpolicy="no-referrer"
    />
    <nav
      class="relative flex flex-wrap items-center justify-between px-2 py-3 bg-white dark:bg-gray-800 shadow-lg"
    >
      <div
        class="container px-4 mx-auto flex flex-wrap items-center justify-between"
      >
        <div
          class="w-full relative flex justify-between lg:w-auto  px-4 lg:static lg:block lg:justify-start"
        >
          <NuxtLink
            class="text-xl font-bold leading-relaxed inline-block mr-4 py-2 whitespace-nowrap text-dark dark:text-white"
            style="text-decoration:none"
            to="/"
            alt="Prashant Upreti"
            title="Prashant Upreti"
          >
            <span class="text-dark dark:text-white">
              <i class="fa-solid fa-flag-usa"></i>rashant
              <i class="fa-solid fa-magnet"></i>preti
            </span>
          </NuxtLink>
          <button
            class="text-dark dark:text-white cursor-pointer text-xl leading-none px-3 py-1 border border-solid border-transparent rounded bg-transparent block lg:hidden outline-none focus:outline-none"
            type="button"
            v-on:click="toggleNavbar()"
          >
            <i class="fas fa-bars"></i>
          </button>
        </div>
        <div
          v-bind:class="{ hidden: !showMenu, flex: showMenu }"
          class="lg:flex lg:flex-grow items-center"
        >
          <ul class="flex flex-col lg:flex-row list-none ml-auto">
            <li class="nav-item lg:border-r">
              <NuxtLink
                class="px-3 py-2 flex items-center text-md  font-bold leading-snug text-dark dark:text-white hover:opacity-75"
                to="/about"
              >
                <i
                  class="fa-solid fa-person-circle-question text-lg leading-lg text-dark dark:text-white opacity-75"
                /><span class="ml-2">About Me</span>
              </NuxtLink>
            </li>
            <li class="nav-item lg:border-r">
              <NuxtLink
                class="px-3 py-2 flex items-center text-md  font-bold leading-snug text-dark dark:text-white hover:opacity-75"
                to="/education"
              >
                <i
                  class="fa-solid fa-graduation-cap text-lg leading-lg text-dark dark:text-white opacity-75"
                /><span class="ml-2">Education</span>
              </NuxtLink>
            </li>
            <li class="nav-item lg:border-r">
              <NuxtLink
                class="px-3 py-2 flex items-center text-md  font-bold leading-snug text-dark dark:text-white hover:opacity-75"
                to="/experience"
              >
                <i
                  class="fa-solid fa-star text-lg leading-lg text-dark dark:text-white opacity-75"
                /><span class="ml-2">Experience</span>
              </NuxtLink>
            </li>
            <li class="nav-item lg:border-r">
              <NuxtLink
                class="px-3 py-2 flex items-center text-md  font-bold leading-snug text-dark dark:text-white hover:opacity-75"
                to="/skills"
              >
                <i
                  class="fa-solid fa-dumbbell text-lg leading-lg text-dark dark:text-white opacity-75"
                /><span class="ml-2">Skills</span>
              </NuxtLink>
            </li>
            <li class="nav-item lg:border-r">
              <NuxtLink
                class="px-3 py-2 flex items-center text-md  font-bold leading-snug text-dark dark:text-white hover:opacity-75"
                to="/scholarships"
              >
                <i
                  class="fa-solid fa-handshake-angle text-lg leading-lg text-dark dark:text-white opacity-75"
                /><span class="ml-2">Scholarships</span>
              </NuxtLink>
            </li>
            <li class="nav-item lg:border-r">
              <NuxtLink
                class="px-3 py-2 flex items-center text-md  font-bold leading-snug text-dark dark:text-white hover:opacity-75"
                to="/languages"
              >
                <i
                  class="fa-solid fa-language text-lg leading-lg text-dark dark:text-white opacity-75"
                /><span class="ml-2">Languages</span>
              </NuxtLink>
            </li>
            <li class="nav-item lg:border-r">
              <a
                class="px-3 py-2 flex items-center text-md  font-bold leading-snug text-dark dark:text-white hover:opacity-75"
                onclick="return confirm('Do you want to download Prashant\'s Resume?')"
                href="/Prashant_Upreti_Resume.pdf"
                download
              >
                <i
                  class="fa-solid fa-download text-lg leading-lg text-dark dark:text-white opacity-75"
                /><span class="ml-2">Download</span>
              </a>
            </li>
            <li class="nav-item lg:border-r">
              <a
                class="px-3 py-2 flex items-center text-md  font-bold leading-snug text-blue-600 hover:opacity-75"
                href="https://www.linkedin.com/in/prashant-upreti"
                target="_blank"
              >
                <i
                  class="fa-brands fa-linkedin text-lg leading-lg opacity-75"
                /><span class="ml-2 mr-2">LinkedIn</span>
                <i class="fa fa-external-link" aria-hidden="true"></i>
              </a>
            </li>            
            <li class="nav-item lg:border-r">
              <a
                class="px-3 py-2 flex items-center text-md  font-bold leading-snug text-blue-600 hover:opacity-75"
                href="https://github.com/prashantupreti"
                target="_blank"
              >
                <i
                  class="fa-brands fa-github text-lg leading-lg opacity-75"
                /><span class="ml-2 mr-2">GitHub</span>
                <i class="fa fa-external-link" aria-hidden="true"></i>
              </a>
            </li>
            <li class="nav-item">
              <button
                class="px-3 py-2 flex items-center text-md  font-bold leading-snug text-dark dark:text-white hover:opacity-75"
                type="button"
                @click="toggleTheme()"
              >
                <i
                  class="fa-solid fa-sun text-lg leading-lg opacity-75"
                  v-show="!isDark"
                ></i>
                <i
                  class="fa-solid fa-moon text-lg leading-lg opacity-75"
                  v-show="isDark"
                ></i>
              </button>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </div>
</template>
<style scoped>
a.nuxt-link-active,
a.nuxt-link-exact-active {
  text-decoration: underline;
}
</style>
<script>
export default {
  name: 'Navbar',
  data () {
    return {
      showMenu: false,
      isDark: false
    }
  },
  methods: {
    toggleNavbar: function () {
      this.showMenu = !this.showMenu
    },
    toggleTheme: function () {
      this.isDark = !this.isDark
      if (process.client) localStorage.setItem('isDark', this.isDark)
    }
  },
  watch: {
    isDark (currentValue) {
      this.$emit('update', currentValue)
    }
  },
  beforeMount () {
    this.$emit('update', this.isDark)
    this.isDark = process.client
      ? JSON.parse(localStorage.getItem('isDark'))
      : false
  }
}
</script>
