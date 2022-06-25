<template>
  <div>
    <Header
      v-bind:image="image"
      title="Experience"
      icon="fa-solid fa-star"
      subtitle=""
    />
    <div
      class="divide-y divide-gray-600 dark:divide-white divide-solid md:divide-none"
    >
      <div v-for="(experience, index) in experiences" :key="index">
        <ExpTemplate
          :exp_details="experience.exp_details"
          :exp_title="experience.exp_title"
          :from_to="experience.from_to"
          :exp_for="experience.exp_for"
          :exp_media="experience.exp_media"
          :img_order="experience.img_order"
          :detail_order="experience.detail_order"
          :exp_icon="experience.exp_icon"
          :exp_icon_bg="experience.exp_icon_bg"
          :exp_icon_text="experience.exp_icon_text"
        />
      </div>
    </div>
  </div>
</template>
<script>
import img from 'assets/img/experience.webp'
export default {
  data () {
    return {
      image: img,
      experiences: [
        {
          exp_details: [
            'Built an Android App in JAVA using Android Studio',
            'Used C-programming in Raspberry Pi to get data from sensors every minute',
            'Inserted data to a MySQL database using a REST API POST URL and PHP scripts',
            'Android App was used as a GUI to read that live fed data through the REST API GET link'
          ],
          exp_title: 'Home-Weather Station',
          from_to: 'August 2021-December 2021',
          exp_for: 'Project Lab III',
          exp_media: require('~/assets/media/android_app.gif'),
          img_order: '',
          detail_order: '',
          exp_icon: 'fa-solid fa-bolt',
          exp_icon_bg: 'bg-blue-300',
          exp_icon_text: 'text-blue-600'
        },
        {
          exp_details: [
            'Learned Laravel MVC Framework to create productive web applications',
            'Trained on integrating Laravel with Vue.js, Tailwind CSS, and Bootstrap',
            'Designed interactive admin dashboards to control perform various CRUD tasks in web applications',
            'Experienced in mixing WebSocket, using REST API on Laravel, and working with WP REST API',
            'Built a website with best SEO score and great UX performance'
          ],
          exp_title: 'Full Stack Developer',
          from_to: 'August 2017-Present',
          exp_for: 'Personal Projects',
          exp_media: require('~/assets/img/bgnepali.webp'),
          img_order: 'md:order-2',
          detail_order: 'md:order-1',
          exp_icon: 'fa-solid fa-laptop-code',
          exp_icon_bg: 'bg-green-300',
          exp_icon_text: 'text-green-800'
        },
        {
          exp_details: [
            'Used OpenCV with Python via Raspberry Pi and the Pi Camera module to capture the license plate',
            'Designed GUI to save license plate into MariaDB using python scripts and SQL commands',
            'Used that entry from MariaDB to compare the license plate picture from Pi Camera module',
            'On successful comparison a DC motor was ran'
          ],
          exp_title: 'License Plate Detection',
          from_to: 'June 2021-August 2021',
          exp_for: 'Project Lab II',
          exp_media: require('~/assets/media/license_plate_project.gif'),
          img_order: 'w-72',
          detail_order: '',
          exp_icon: 'fa-solid fa-eye',
          exp_icon_bg: 'bg-yellow-300',
          exp_icon_text: 'text-yellow-900'
        },
        {
          exp_details: [
            'Designed and updated homepage of University Advising Office and other departments under it',
            'Updated the Virtual Fair website of Pre-Professional Health Careers department using the Omni CMS',
            'Generated HTML tags by programming in Laravel and using a MySQL database for the Virtual Fair site',
            'Designed the homepage of Tech Transfer Acceleration Program using HTML, CSS, and jQuery',
            'Responsible for updating contents and medias in other webpages of University Advising'
          ],
          exp_title: 'Web Development',
          from_to: 'October 2020-May 2022',
          exp_for: 'University Advising',
          exp_media: require('~/assets/media/ua.gif'),
          img_order: 'md:order-2',
          detail_order: 'md:order-1',
          exp_icon: 'fa-solid fa-desktop',
          exp_icon_bg: 'bg-red-300',
          exp_icon_text: 'text-red-800'
        },
        {
          exp_details: [
            'Performed filing and data-management task',
            'Assisted patrons with references and resources',
            'Locate, retrieve and reshelve materials requested by patrons',
            'Received phone calls and addressed questions and concerns',
            'Updated the website for reference files'
          ],
          exp_title: 'Student Assistant',
          from_to: 'November 2018-May 2020',
          exp_for: 'Southwest Collection/Special Collection Library',
          exp_media: require('~/assets/img/swco.webp'),
          img_order: 'w-72',
          detail_order: '',
          exp_icon: 'fa-solid fa-book-bookmark',
          exp_icon_bg: 'bg-indigo-300',
          exp_icon_text: 'text-indigo-900'
        },
        // {
        //   exp_details: [
        //     'Designed and updated homepage of University Advising Office and other departments under it',
        //     'Updated the Virtual Fair website of Pre-Professional Health Careers department using the Omni CMS',
        //     'Generated HTML tags by programming in Laravel and using a MySQL database for the Virtual Fair site',
        //     'Designed the homepage of Tech Transfer Acceleration Program using HTML, CSS, and jQuery',
        //     'Responsible for updating contents and medias in other webpages of University Advising'
        //   ],
        //   exp_title: 'Web Development',
        //   from_to: 'October 2020-May 2022',
        //   exp_for: 'University Advising',
        //   exp_media: require('~/assets/media/ua.gif'),
        //   img_order: 'md:order-2',
        //   detail_order: 'md:order-1',
        //   exp_icon: 'fa-solid fa-desktop',
        //   exp_icon_bg: 'bg-red-300',
        //   exp_icon_text: 'text-red-800'
        // }
      ]
    }
  },
  head: {
    title: 'Experience - Prashant Upreti',
    meta: [
      {
        hid: 'description',
        name: 'description',
        content: 'Experience Page'
      }
    ]
  }
}
</script>
