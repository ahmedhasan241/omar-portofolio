<script setup >
import 'swiper/swiper-bundle.css';
const props = defineProps({

  description: { type: String, required: true },
  imgUrl: { type: Array, required: true },

});


</script>

<template>
  <div class="shadow-xl transition-all  hover:shadow-primary">
    <div class=" rounded-t-xl overflow-hidden relative group">
            <img
  v-if="imgUrl.length === 1 && typeof imgUrl[0] === 'string'"
  :src="imgUrl[0]"
  alt="Project Image"
  class="w-full h-full object-cover"
      />

  <div v-else>

      <div id="carouselExampleAutoplaying" class="carousel slide" data-bs-ride="carousel">
  <div class="carousel-inner">
    <div class="carousel-item active" >
      <img          
          :src="imgUrl[0]" 
          alt="Project Image"  class="d-block w-100" >
    </div>

    <div class="carousel-item " v-for="(img, index) in imgUrl.slice(1)" :key="index">
      <img           v-if="typeof img === 'string'" 
          :src="img" 
          alt="Project Image"  class="d-block w-100" >
    </div>
  </div>
  <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleAutoplaying" data-bs-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Previous</span>
  </button>
  <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleAutoplaying" data-bs-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Next</span>
  </button>
</div>
    <!-- <swiper
      :slides-per-view="1"
      space-between="30"
      navigation
      pagination
      loop
      class="mySwiper"
    >
      Loop through the imgUrl array and display each image
      <swiper-slide v-for="(img, index) in imgUrl" :key="index">
        <img 
          v-if="typeof img === 'string'" 
          :src="img" 
          alt="Project Image" 
          class="w-full h-full object-cover"
        />
      </swiper-slide>
    </swiper> -->
  </div>
    </div>
    <div class="rounded-b-xl mt-1 py-3 md:!py-6  px-2 md:!px-6">
      <p class="dark:text-[#ADB7BE] text-slate-800" v-html="description">

      </p>
      <p v-html="description"></p>

    </div>
  </div>
</template>
