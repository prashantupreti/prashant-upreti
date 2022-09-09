<template>
  <Section>
    <div class="grid md:grid-cols-3">
      <div :class="img_order" class="ml-auto mr-auto">
        <img
          :alt="exp_title"
          class="max-w-full rounded-lg shadow-2xl h-96 object-cover"
          :src="exp_media"
        />
      </div>
      <div :class="detail_order" class="mt-4 md:mt-0 col-span-2">
        <div class="md:pr-12">
          <div class="flex">
            <div
              class="p-3 text-center inline-flex items-center justify-center w-16 h-16 mb-6 shadow-lg rounded-full"
              :class="exp_icon_bg + ' ' + exp_icon_text"
            >
              <i :class="exp_icon" class="text-xl"></i>
            </div>
            <p class="p-3 text-center mt-2">
              <i>{{ exp_for }}</i> &middot; {{ from_to }}
            </p>
          </div>
          <h3 class="text-3xl font-semibold">{{ exp_title }}</h3>
          <ul class="fa-ul" v-for="(detail, index) in exp_details" :key="index">
            <li class="text-left mt-2">
              <span class="fa-li"><i class="fa-solid fa-code"></i></span
              >{{ detail }}
            </li>
          </ul>
        </div>
      </div>
    </div>
  </Section>
</template>
<script>
export default {
  props: [
    'exp_details',
    'exp_title',
    'from_to',
    'exp_for',
    'exp_media',
    'img_order',
    'detail_order',
    'exp_icon',
    'exp_icon_bg',
    'exp_icon_text'
  ]
}
</script>
