

<template>
  <section id="about" class="flex flex-col gap-10 py-4 sm:pb-10">
    <div
      class="flex p-0.5 relative w-[150px] md:w-[350px] h-[150px] md:h-[350px] rounded-full mx-auto"
      v-motion-fade-visible-once
    >
      <div
        class="absolute inset-0 overflow-hidden rounded-full flex items-center justify-center"
      >
        <div
          class="bg-gradient-to-r absolute inset-[-20px] from-cyan-400 to-primary specialSpin"
        />
      </div>

      <img
        loading="eager"
        src="https://i.postimg.cc/rpz1H1MC/IMG-3447.jpg"
        alt="programming"
        class="w-full h-full rounded-full object-cover z-[2]"
      />
    </div>
    <div class="flex flex-col text-center gap-2 md:gap-4 lg:gap-5">
      <div class="flex items-center justify-center space-x-4">
  <h1 class="text-4xl font-bold ">Omar Elbakry</h1>

</div>
      <h1 class="font-semibold text-xl sm:text-2xl md:text-3xl">
      Performance Media Buyer
      </h1>
      <p class="text-center md:!text-center  text-md sm:text-lg md:text-xl text-balance mx-0  md:!mx-32">
        I am a seasoned <span class="!text-bolder">Performance Media Buyer</span> with extensive experience spanning several
        years within the Digital Marketing industry. My expertise encompasses a
        comprehensive understanding of paid advertising strategies, which I adeptly apply
        to achieve business objectives and foster growth while maximizing Return on Ad
        Spend (ROAS) and Return on Investment (ROI). Throughout my career, I have
        cultivated a profound comprehension of online digital sales, enabling me to
        orchestrate successful Projects across various platforms including: (Facebook –
        Instagram – TikTok – Snapchat – Google) 
        <br>
        <br>
        My proficiency extends across diverse
        industries such as: (E-commerce – Services – Medical –– Food & Beverage)
      </p>
      <div class="mx-0 md:!mx-32">
 <div class="w-full  mx-auto mt-10 space-y-2">
    <div v-for="(item, index) in accordions" :key="index">
      <!-- Accordion Header -->
      <div class="accordion-header border-b border-gray-200 cursor-pointer flex justify-between items-center" @click="toggleAccordion(index)">
        <h2 class="text-lg font-medium p-4">{{ item.title }}</h2>
        <!-- Arrow Icon -->
        <svg
          :class="{'rotate-180': activeIndex === index}"
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6 transition-transform duration-300 transform"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
        </svg>
      </div>
      <!-- Accordion Body with Transition -->
      <transition name="accordion">
       <div v-if="activeIndex === index" class="accordion-body">
          <!-- v-html to render the HTML content for each accordion -->
          <div class="px-1 py-3 md:p-4 dark:text-white text-gray-700" v-html="item.content"></div>
        </div>
      </transition>
    </div>
  </div>
      </div>

    </div>
  </section>
</template>
<script setup>
import { ref } from 'vue'

// Sample accordion data

// Sample accordion data
const accordions = ref([
  {title: 'Education', content: `
      <ul class="list-disc pl-5 mx-2 md:mx-4 space-y-2  !text-start">
      <li >I studied <strong>Journalism</strong> at the College of Arts, Mass Communication Department, 
    <strong>Mansoura University</strong>.</li>

    </ul>
    <p class="!text-start"></p>
  `},
  { title: 'Experience', content: `
    <ul class="list-disc pl-5 mx-2 md:mx-4 space-y-2  !text-start">
      <li class="font-bold"><span class="font-normal">Marketing Specialist</span> ( Mhmrh Mqmrh (KSA) )</li>
      <li class="font-bold"><span class="font-normal">Performance Media Buyer</span> ( Pink Pharmacy (KSA) )</li>
      <li class="font-bold"><span class="font-normal">Performance Media Buyer</span> ( Ch&Be (EGY) )</li>
      <li class="font-bold"><span class="font-normal">Performance Media Buyer</span> ( TAR Company (EGY) )</li>
    </ul>` 
  },
  { title: 'Courses', content:  `
    <ul class="list-disc pl-5 mx-2 md:mx-4  !text-start font-bold space-y-2 ">
      <li>Media Buyer Mind Shift</li>
      <li>Digital Marketing Diploma</li>
      <li>E-gulf Course for E-commerce in Gulf countries</li>
    </ul>`  },
  { title: 'Skills', content: `
    <ul class="list-disc pl-5 mx-2 md:mx-4 !text-start space-y-2 ">
      <li>Ads Copywriting</li>
      <li>Facebook tracking and analytics tools</li>
      <li>Facebook testing, scaling and retargeting</li>
      <li>Ads retargeting</li>
      <li>Google Analytics</li>
      <li>Google Looker Studio</li>
      <li>TikTok Ads</li>
      <li>Snapchat Ads</li>
      <li>Google Ads</li>
    </ul>`  },
  { title: 'Languages', content: `
    <ul class="list-disc pl-5 mx-2 md:mx-4 text-start space-y-2 ">
      <li>Arabic (Mother Tongue)</li>
      <li>English (Good command spoken and writing)</li>
    </ul>`  }
])

const activeIndex = ref(null)

// Toggle accordion
const toggleAccordion = (index) => {
  activeIndex.value = activeIndex.value === index ? null : index
}
</script>

<style scoped>
.accordion-enter-active, .accordion-leave-active {
  transition: all 0.5s ease;
}
.accordion-enter-from, .accordion-leave-to {
  max-height: 0;
  opacity: 0;
}
.accordion-enter-to, .accordion-leave-from {
  max-height: 1000px;
  opacity: 1;
}
</style>