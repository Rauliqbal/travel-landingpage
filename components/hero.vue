<script setup>
</script>
<template>
  <section class="max-container padding-container flex flex-col gap-20 py-10 pb-32 md:gap-28 lg:py-20 xl:flex-row">
    <div class="hero-map"></div>
    <div class="relative z-20 flex flex-1 flex-col xl:w-1/2">
      <NuxtImg src="/img/camp.svg" class="absolute -left-[5px] -top-[30px] w-10 lg:w-[50px]" width="50" height="50" placeholder/>
      <h1 class="bold-52 lg:bold-88">Putuk Truno Camp Area</h1>
      <p className="regular-16 mt-6 text-gray-30 xl:max-w-[520px]">
        We want to be on each of your journeys seeking the satisfaction of seeing the incorruptible beauty of nature. We can help you on an adventure around the world in just one app
      </p>
      <div class="my-11 flex flex-wrap gap-5">
        <div class="flex items-center gap-2">
          <div v-for="icon in 5" :key="icon">
            <NuxtImg src="/img/star.svg" width="24" height="24"/>
          </div>
        </div>
        <p class="bold-16 lg:bold-20 text-blue-70">
          198K
          <span class="regular-15 lg:regular-20 ml-1">
            Excellent Reviews
          </span>
        </p>
      </div>

      <div class="flex flex-col sm:flex-row w-full gap-3">
      <Button title="Download App" variant="btn_green"/>
      <Button icon="play.svg" title="Download App" variant="btn_white_text"/>
      </div>
    </div>
    <div class="flex flex-1 items-start">
      <div class="bg-green-90 flex flex-col gap-8 px-7 py-8 rounded-3xl w-[268px] z-20">
        <div class="flex flex-col">
          <div class="flexBetween">
            <p class="text-gray-20 regular-16">
              Location
            </p>
            <NuxtImg src="/img/close.svg" width="24" height="24"/>
          </div>
        </div>
      </div>    </div>
  </section>
</template>