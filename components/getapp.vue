<script setup>
</script>
<template>
  <section class="flexCenter w-full flex-col pb-[100px]">
    <div class="get-app">
      <div class="z-20 flex w-full flex-1 flex-col items-start justify-center gap-12">
        <h2 class="bold-40 lg:bold-64 xl:max-w-[320px]">Get for free now!</h2>
        <p class="regular-16 text-gray-10">Available on iOS and Android</p>
        <div class="flex w-full flex-col gap-3 whitespace-nowrap xl:flex-row">
          <Button 
            type="button"
            title="App Store"
            icon="/apple.svg"
            variant="btn_white w-full"
            full
          />
          <Button 
            type="button"
            title="Play Store"
            icon="/android.svg"
            variant="btn_dark_green_outline w-full"
            full
          />
        </div>
      </div>

      <div class="flex flex-1 items-center justify-end">
        <NuxtImg src="/img/phones.png" alt="phones" width="550" height="870" />
      </div>
    </div>
  </section>
</template>