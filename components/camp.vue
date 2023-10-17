<script setup>
import {PEOPLE_URL} from "../data/utils.ts"

const bgImage = [
  {
    title: "Putul Truno Camp",
    subtitle : "Prigen, Pasuruan",
    backgroundImage: "bg-camp-1"
  },
  {
    title: "Putul Truno Camp",
    subtitle : "Prigen, Pasuruan",
    backgroundImage: "bg-camp-2"
  }
]
</script>
<template>
  <section class="2xl:max-container relative flex flex-col py-10 lg:mb-10 lg:py-20 xl:mb-20">
    <div class="hide-scrollbar flex h-[340px] w-full items-start justify-start gap-8 overflow-x-auto lg:h-[400px] xl:h-[640px]">

      <div v-for="camp in bgImage" :key="camp" :class="camp.backgroundImage + ' w-full h-full min-w-[1100px] bg-cover bg-no-repeat lg:rounded-r-5xl 2xl:rounded-5xl'">
        <div class="flex h-full flex-col items-start justify-between p-6 lg:px-20 lg:py-10">
          <div class="flexCenter gap-4">
            <div class="rounded-full bg-green-50 p-4">
              <NuxtImg src="/img/folded-map.svg" width="28" height="28"/>
            </div>
            <div class="flex flex-col gap-1">
              <h4 class="bold-18 text-white">
                {{ camp.title }}
              </h4>
              <p class="regular-14 text-white">
                {{ camp.subtitle }}
              </p>
            </div>
          </div>

          <div class="flexCenter gap-6">
            <span class="flex -space-x-4 overflow-hidden">
              <div v-for="user in PEOPLE_URL" :key="user">
                <NuxtImg class="inline-block" :src="'/img/' +user" width="52" height="52"/>
              </div>
            </span>
            <p class="bold-16 md:bold-20 text-white">50+ Joined</p>
          </div>
        </div>
      </div>
    </div>

    <div class="flexEnd mt-10 lg:-mt-60 px-6 lg:mr-6">
      <div class="bg-green-50 p-8 lg:max-w-[500px] xl:max-w-[734px] xl:rounded-5xl xl:px-16 xl:py-20 relative w-full overflow-hidden rounded-3xl">
        <h2 class="regular-24 md:regular-32 2xl:regular-64 capitalize text-white">
          <strong>Feeling Lost</strong> and not knowing the way ?
        </h2>

        <p class="regular-14 xl:regular-16 mt-5 text-white">
          Starting from the anxiety of the climbers when visiting a new climbing location, the possibility of getting lost is very large. That's why we are here for those of you who want to start an adventure
        </p>
        <NuxtImg src="/img/quote.svg" class="camp-quote" width="186" height="219"/>
      </div>
    </div>

  </section>
</template>