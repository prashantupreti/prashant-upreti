<template>
  <div :class="isDark ? 'dark' : ''">
    <Navbar @update="isDark = $event" />
    <Nuxt />
    <Footer />
  </div>
</template>
<style>
@import url('https://fonts.googleapis.com/css2?family=Lato:wght@100;400&display=swap');
html {
  scroll-behavior: smooth !important;
  font-family: 'Lato', sans-serif;
}
</style>
<script>
export default {
  data(){
    return{
      isDark: false,
    }
  },
  beforeMount(){
    this.isDark = (process.client) ? JSON.parse(localStorage.getItem('isDark')) : false;
  }
}
</script>
