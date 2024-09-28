<script setup lang="ts">
import { Projects } from '@/data/constants'
</script>

<template>
  <section
    class="mt-20 flex flex-col gap-24"
    id="Campaigns">
    <div class="flex flex-col gap-2 text-center">
      <h4 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        Campaigns Results
      </h4>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-14">
      <ProjectCard
        v-for="project in Projects"
        :key="project.id"
        :title="project.title"
        :description="project.description"
        :imgUrl="project.image"
        :gitUrl="project.gitUrl"
        :previewUrl="project.previewUrl" />
    </div>
  </section>
</template>
