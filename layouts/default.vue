<template>
  <div :class="isDark ? 'dark' : ''">
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Lato&display=swap"
      rel="stylesheet"
    />
    <Navbar @update="isDark = $event" />
    <Nuxt />
    <Footer />
  </div>
</template>
<style>
html {
  scroll-behavior: smooth !important;
  font-family: 'Lato', sans-serif !important;
}
</style>
<script>
export default {
  data () {
    return {
      isDark: false
    }
  },
  beforeMount () {
    this.isDark = process.client
      ? JSON.parse(localStorage.getItem('isDark'))
      : false
  }
}
</script>
