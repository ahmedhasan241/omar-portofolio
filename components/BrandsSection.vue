<template>
    <div class="py-20 bg-[#F8FAFC]">
  <div id="Brands" >
    <div class="flex justify-center mb-8">
        <h2 class="text-black font-bold text-xl lg:text-5xl">Brands I Have Worked With:</h2>
    </div>
    <Swiper
      :slides-per-view="6"
        space-between="0"
        :breakpoints="{
          320: {
            slidesPerView: 2,
            spaceBetween: 10,
          },
          768: {
            slidesPerView: 4,
            spaceBetween: 0,
          },
          1024: {
            slidesPerView: 6,
            spaceBetween: 0,
          },
        }"
        class="mySwiper max-w-[1200px] w-full px-3 md:px-0"
        loop="true"

    >
      <SwiperSlide v-for="(client, index) in clients" :key="index" clas>
        <img :src="client" alt="Client Logo" class="border-4 border-black  rounded-full w-40 h-36 md:h-40" />
      </SwiperSlide>
    </Swiper>
  </div>
  <div id="Tools" class="px-2 md:!px-10 lg:!px-40 mt-20 pt-20 ">
    <div class="flex justify-center md:justify-start">
        <h2 class="text-center md:!text-start text-black font-extrabold !text-xl md:!text-3xl lg:!text-5xl">TOOLS WORK ON IT AND  <br> <span class="text-center md:!text-start">EXPERT <span class="text-primary">MMP</span>.</span></h2>
    </div>
    <div class="mx-auto grid grid-cols-2 md:grid-cols-3  lg:grid-cols-4 lg:gap-10 xl:grid-cols-5">
        <div v-for="(tool , index) in tools" :key="index" class=" flex justify-center p-4">
            <img :src="tool" class="w-full h-full" alt="">
        </div>
    </div>
  </div></div>
</template>

<script setup>
import { ref } from 'vue';
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/swiper-bundle.css';

const clients = ref([
  "https://i.postimg.cc/3wvkVyX4/client-1.webp",
  "https://i.postimg.cc/qMvz0Dcd/client-2.jpg",
  "https://i.postimg.cc/Y97CPd2Z/client-3.png",
  "https://i.postimg.cc/8PcPxJDp/client-4.jpg",
  "https://i.postimg.cc/XqJ4MhRH/client-5.avif",
  "https://i.postimg.cc/kGp97s9n/client-6.webp",
  "https://i.postimg.cc/J4sMPfct/client-7.png",
  "https://i.postimg.cc/Fz8tMKgz/client-8.png",
  "https://i.postimg.cc/W1MRyTDp/client-9.png",
  "https://i.postimg.cc/fy6FHrD0/client-10.avif"
]);

const tools = ref([
  "https://i.postimg.cc/NGkZRByR/tool-1.jpg",
  "https://i.postimg.cc/wTxZVZJZ/tool-2.png",
  "https://i.postimg.cc/5NPGkgS0/tool-3.jpg",
  "https://i.postimg.cc/fLhg0rDH/tool-4.png",
  "https://i.postimg.cc/pLh0cHdG/tool-5.png",
  "https://i.postimg.cc/DwksFkgY/tool-6.png",
  "https://i.postimg.cc/WpdX1VG2/tool-10.png",
  "https://i.postimg.cc/66Fz7PcC/tool-7.png",
  "https://i.postimg.cc/kgmcstk4/tool-8.png",
  "https://i.postimg.cc/c4Yhfck2/tool-9.png"
]);
</script>

<style scoped>
.mySwiper {
  width: 100%;
  height: 100%;
}
</style>
