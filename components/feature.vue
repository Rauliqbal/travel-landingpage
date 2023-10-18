<script setup>
import { FEATURES } from '~/data/utils';
</script>
<template>
<section class="flex-col flexCenter overflow-hidden bg-feature bg-center bg-no-repeat py-24">
  <div class="max-container padding-container relative w-full flex justify-end">
    <div class="flex flex-1 lg:min-h-[900px]">
      <NuxtImg src="/img/phone.png" width="440" class="feature-phone"/>
    </div>

    <div class="z-20 flex w-full flex-col lg:w-[60%]">
      <div class="relative">
        <NuxtImg src="/img/camp.svg" width="50" height="50" class="absolute left-[-5px] top-[-28px] w-10 lg:w-[50px]"/>
        <h2 class="bold-40 lg:bold-64">Our Features</h2>
      </div>

      <ul class="mt-10 grid gap-10 md:grid-cols-2 lg:mg-20 lg:gap-20">
        <li v-for="feature in FEATURES" :key="feature" class="flex w-full flex-1 flex-col items-start">
          <div class="rounded-full p-4 lg:p-7 bg-green-50">
            <NuxtImg :src="'/img/'+feature.icon" alt="map" width="28" height="28" />
          </div>
          <h2 class="bold-20 lg:bold-32 mt-5 capitalize">
            {{feature.title}}
          </h2>
          <p class="regular-16 mt-5 bg-white/80 text-gray-30 lg:mt-[30px] lg:bg-none">
            {{feature.description}}
          </p>
        </li>
      </ul>
    </div>
  </div>
</section>
</template>