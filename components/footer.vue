<script setup>
import { SOCIALS } from "~/data/utils";
import { FOOTER_CONTACT_INFO, FOOTER_LINKS } from "~/data/utils";
</script>
<template>
  <footer class="flex-center mb-24">
    <div class="padding-container max-container flex w-full flex-col gap-14">
      <div
        class="flex flex-col items-start justify-center gap-[10%] md:flex-row"
      >
        <NuxtLink to="/" class="mb-10">
          <NuxtImg src="/img/hilink-logo.svg" width="74" height="29" />
        </NuxtLink>

        <div class="flex flex-wrap gap-10 sm:justify-between md:flex-1">
          <div v-for="columns in FOOTER_LINKS" class="flex flex-col gap-5">
            <h4 class="bold-18 whitespace-nowrap">{{ columns.title }}</h4>
            <ul class="regular-14 flex flex-col gap-4 text-gray-30">
              <NuxtLink to="/" v-for="links in columns.links">{{
                links
              }}</NuxtLink>
            </ul>
          </div>

          <div
            v-for="columns in FOOTER_CONTACT_INFO"
            class="flex flex-col gap-5"
          >
            <h4 class="bold-18 whitespace-nowrap">{{ columns.title }}</h4>
            <ul class="regular-14 flex flex-col gap-4 text-gray-30">
              <NuxtLink
                v-for="links in columns.links"
                to="/"
                class="flex gap-4 md:flex-col lg:flex-row"
                ><p className="whitespace-nowrap">
                  {{ links.label }}
                </p>
                <p className="medium-14 whitespace-nowrap text-blue-70">
                  {{ links.value }}
                </p></NuxtLink
              >
            </ul>
          </div>

          <div v-for="columns in SOCIALS" class="flex flex-col gap-5">
            <h4 class="bold-18 whitespace-nowrap">{{ columns.title }}</h4>
            <ul class="regular-14 flex gap-4 text-gray-30">
              <NuxtLink to="/" v-for="links in columns.links"
                ><NuxtImg :src="'/img/' + links" width="24" height="24"
              /></NuxtLink>
            </ul>
          </div>
        </div>
      </div>
      <div className="border bg-gray-20" />
      <p className="regular-14 w-full text-center text-gray-30">
        2023 Hilink | All rights reserved
      </p>
    </div>
  </footer>
</template>
