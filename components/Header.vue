<template>
  <div
    class="relative pt-16 pb-32 flex content-center items-center justify-center"
    style="min-height: 75vh;"
    id="about"
  >
    <div
      class="absolute top-0 w-full h-full bg-center bg-cover"
      :style="{ backgroundImage: `url(${image})` }"
    >
      <span
        id="blackOverlay"
        class="w-full h-full absolute opacity-75 bg-black"
      ></span>
    </div>
    <div class="container relative mx-auto">
      <div class="items-center">
        <div class="w-full px-4 ml-auto mr-auto text-center">
          <div class="flex">
            <div class="flex-auto w-80 ">
              <h1
                class="text-white font-semibold text-4xl md:text-7xl uppercase tracking-wide"
              >
                <i :class="icon"></i> {{ title }}
              </h1>

              <h4 class="mt-2 text-2xl text-white">
                {{ subtitle }}
              </h4>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- <div
      class="top-auto bottom-0 left-0 right-0 w-full absolute pointer-events-none overflow-hidden"
      style="height: 70px;"
    >
      <svg
        class="absolute bottom-0 overflow-hidden"
        xmlns="http://www.w3.org/2000/svg"
        preserveAspectRatio="none"
        version="1.1"
        viewBox="0 0 2560 100"
        x="0"
        y="0"
      >
        <polygon
          class="text-gray-200 fill-current"
          points="2560 0 2560 100 0 100"
        ></polygon>
      </svg>
    </div> -->
  </div>
</template>
<script>
export default {
  props: ['image', 'title', 'icon', 'subtitle']
}
</script>
