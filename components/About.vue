<template>
  <div>
    <Header
      v-bind:image="image"
      title="About Me"
      icon="fa-solid fa-person-circle-question"
      subtitle=""
    />
    <Section class="text-xl md:text-lg leading-relaxed text-justify">
      <p class="py-4">
        <span class="text-6xl">W</span>elcome to my portfolio site. I am Prashant Upreti, a student of BS in
        Computer Engineering at Texas Tech University graduating this August
        2022. I have learned a lot of programming languages during my academic
        career here at Texas Tech but also have been learning more on the side
        along my coursework.
      </p>
      <p class="py-4">
        I have two years of experience maintaining websites for the University
        Advising department of Texas Tech University as a part time student
        employee. In this interval I have grown my programming skills to a new
        level by getting involved in many projects. For example, once one of the
        departments of University Advising wanted to design an informative
        website for their Virtual Health Fair and they had a big excel files
        with records of universities and their contact. I was given the job to
        find out a way to display that large excel files in a webpage using
        HTML, CSS, and jQuery. I was able to import that excel file into a MySQL
        database and then use Laravel framework to generate HTML tags so that
        the data from the excel file will be displayed as they wanted. This is
        one of my achievements. Also, I was involved in designing the homepage
        of University Advising and Tech Transfer Acceleration Program&nbsp;and
        making various updates around other pages within the department.
      </p>
      <p class="py-4">
        I have also worked in upgrading a Unity game project in a group this
        Spring for Project Lab IV, developed android application in my group
        project for Project Lab III, worked on a computer vision project last
        summer in a group for Project Lab II, developed an autonomous rover
        using Verilog as a group for Project Lab I. Also, developed an ecommerce
        JAVA application for my Object-Oriented Programming class. On my free
        time I have worked on various Laravel, Vue.js, Nuxt.js, Node.js, React
        Native, Java and Kotlin for android development, and WebSocket&rsquo;s
        projects. <i>Programming is rather a hobby for me than a job/assignment</i>. There is this
        different kind of adrenaline rush when I get to fix a bug in my
        code.
      </p>
      <p class="py-4">
        I have developed this site to show off my talent to my probable
        employer. I hope you check on the Experience tab to check for my
        descriptive experience working on various academic and professional
        projects both as a student and a part time employee for the University
        Advising department.
      </p>
      <p class="py-4">
        Your Sincerely, <br/>
        Prashant Upreti
      </p>
    </Section>
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
