<template>
  <div :class="isDark ? 'dark' : ''">
    <Navbar @update="isDark = $event" />
    <Nuxt />
    <Footer />
  </div>
</template>
<style>
@import url('https://fonts.googleapis.com/css2?family=Nunito:ital,wght@0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
html {
  scroll-behavior: smooth !important;
  font-family: 'Nunito', sans-serif;
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
