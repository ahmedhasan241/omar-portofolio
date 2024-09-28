<script setup lang="ts">
const props = defineProps({

  description: { type: String, required: true },
  imgUrl: { type: String, required: true },

});
</script>

<template>
  <div class="shadow-xl transition-all  hover:shadow-primary">
    <div class=" rounded-t-xl overflow-hidden relative group">
      <img
        :src="imgUrl"
        alt="Project Image"
        class="w-full h-full object-cover "
      />
    </div>
    <div class="rounded-b-xl mt-1 py-3 md:!py-6  px-2 md:!px-6">
      <p class="dark:text-[#ADB7BE] text-slate-800" v-html="description">

      </p>
      <p v-html="description"></p>

    </div>
  </div>
</template>
