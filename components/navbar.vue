<script setup>
function showHide() {
  document.getElementById("hamburger").checked = false;
}

const links = [
  { to: "/", key: "home", label: "Home" },
  { to: "/", key: "how_hilink_work", label: "How Hilink Work?" },
  { to: "/", key: "servicec", label: "Service" },
  { to: "/", key: "pricing", label: "Pricing" },
  { to: "/", key: "contact_us", label: "Contact Us" },
];
</script>

<template>
  <nav class="max-container padding-container py-5">
    <div class="flex items-center justify-between">
      <div class="relative">
        <NuxtLink to="/">
          <img 
            src="/img/hilink-logo.svg"
            alt="Hilink"
            width="72"
            height="20"
          />
          
        </NuxtLink>
      </div>
      <div class="flex items-center">
        <input
          type="checkbox"
          class="peer hidden"
          name="hamburger"
          id="hamburger"
        />
        <label
          for="hamburger"
          class="peer-checked:hamburger z-50 p-4 block cursor-pointer md:hidden"
        >
          <span
            class="transition duration-200 inline-block w-7 h-1 bg-black rounded-xl after:rounded-xl before:rounded-xl"
          ></span>
        </label>
        <div
          @click="showHide"
          class="z-30 absolute inset-0 h-screen bg-gray-900/30 backdrop-blur-sm opacity-0 hidden peer-checked:opacity-100 peer-checked:block transition-all duration-300 md:peer-checked:hidden"
        ></div>
        <div
          class="peer-checked:translate-x-0 w-72 fixed top-0 right-0 bottom-0 translate-x-full transition duration-300 md:w-auto md:static md:translate-x-0 z-40 ease-out"
        >
          <div class="flex flex-col md:items-center md:flex-row h-full">
            <ul
              class="bg-white flex px-7 pt-28 md:pb-0 pb-[38rem] space-y-8 md:px-0 md:space-y-0 flex-col md:flex-row md:space-x-12 md:pt-0"
            >
              <li v-for="link in links" :key="link">
                <NuxtLink
                  @click="showHide"
                  class="text-gray-500 pb-1.5 transition-all hover:font-bold"
                  :to="link.url"
                  >{{ link.label }}</NuxtLink
                >
              </li>
              <li class="md:hidden">
                <Button title="Login" icon="user.svg" variant="bg-[#292c27] text-white"/></li>
            </ul>
          </div>
        </div>
      </div>
      <div class="hidden md:block">
        <Button title="Login" icon="user.svg" variant="bg-[#292c27] text-white"/>
      </div>
    </div>
  </nav>
</template>

<style>
#hamburger ~ label span::after,
#hamburger ~ label span::before {
  background: #000;
  transition-delay: 0.2s, 0s;
  transition-duration: 0.1s;
  transition-property: margin, transform;
  content: "";
  position: absolute;
  width: 28px;
  height: 4px;
}

#hamburger ~ label span::after {
  margin-top: 10px;
}

#hamburger ~ label span::before {
  margin-top: -10px;
}

#hamburger:checked ~ label span {
  background-color: transparent;
}

#hamburger:checked ~ label span:before,
#hamburger:checked ~ label span:after {
  transition-delay: 0s, 0.2s;
  margin-top: 0;
}

#hamburger:checked ~ label span:before {
  transform: rotate(45deg);
}

#hamburger:checked ~ label span:after {
  transform: rotate(-45deg);
}
</style>
