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
            'Coded a backend in PHP and hosted on the internet with POST and GET scripts.',
            'Used C-programming in Raspberry Pi to get data from sensors every minute.',
            'Inserted the collected data to a MySQL database using a REST API POST URL in Raspberry Pi using C.',
            'Developed an Android App in JAVA using Android Studio that acted as a mobile GUI for all live fed data.'
          ],
          exp_title: 'Home-Weather Station Project',
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
            'Made productive web applications using Laravel, Express.js, and Vue.js.',
            'Mastered Laravel and Node.js integration with Vue.js, Tailwind CSS, and Bootstrap.',
            'Chose MySQL and MariaDB for database and skillfully structured and connected tables.',
            'Devised interactive admin dashboards to perform various CRUD functions.',
            'Expert in working with Queues and Scheduler in Laravel and Node.js.',
            'Experienced in mixing WebSocket, using REST APIs on Laravel, and working with WordPress REST APIs.',
            'Built and deployed website with best SEO score and great UX performance.'
          ],
          exp_title: 'Full Stack Developer',
          from_to: 'August 2017-Present',
          exp_for: 'Personal Projects (Self-Motivated)',
          exp_media: require('~/assets/img/bgnepali.webp'),
          img_order: 'md:order-2',
          detail_order: 'md:order-1',
          exp_icon: 'fa-solid fa-laptop-code',
          exp_icon_bg: 'bg-green-300',
          exp_icon_text: 'text-green-800'
        },
        {
          exp_details: [
            'Integrated Pi Camera module with Raspberry Pi to capture an image of a license plate.',
            'Used Tesseract and OpenCV with Python in Raspberry Pi to extract texts from a license plate image.',
            'Constructed GUI to save license plate into MariaDB using Python scripts and SQL commands.',
            'Utilized that entry from MariaDB to compare the license plate number extracted from the image.',
            'On successful comparison a DC motor was ran simulating opening of a gate.'
          ],
          exp_title: 'License Plate Detection Project',
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
            'Designed, developed, and updated homepage of University Advising Office and sub-departments.',
            'Simplified the making of Pre-Professional Health Careers’ Virtual Fair website using Laravel.',
            'Created a responsive homepage for Tech Transfer Acceleration Program using Foundation framework.',
            'Worked on updating the landing page of University Advising’s Orientation webpage.',
            'Responsible for updating contents and medias in other webpages of University Advising.'
          ],
          exp_title: 'Web Developer',
          from_to: 'October 2020-May 2022',
          exp_for: 'University Advising, Texas Tech University',
          exp_media: require('~/assets/media/ua.gif'),
          img_order: 'md:order-2',
          detail_order: 'md:order-1',
          exp_icon: 'fa-solid fa-desktop',
          exp_icon_bg: 'bg-red-300',
          exp_icon_text: 'text-red-800'
        },
        {
          exp_details: [
            'Performed filing and data-management task.',
            'Assisted patrons with references and resources.',
            'Located, retrieved and reshelved materials requested by patrons.',
            'Received phone calls and addressed questions and concerns.',
            'Updated the website for reference files.'
          ],
          exp_title: 'Student Assistant (Customer Service)',
          from_to: 'November 2018-May 2020',
          exp_for: 'Southwest Collection/Special Collection Library',
          exp_media: require('~/assets/img/swco.webp'),
          img_order: 'w-72',
          detail_order: '',
          exp_icon: 'fa-solid fa-book-bookmark',
          exp_icon_bg: 'bg-indigo-300',
          exp_icon_text: 'text-indigo-900'
        }
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
