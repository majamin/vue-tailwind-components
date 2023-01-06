<script setup lang="ts">
import BaseButton from "@/components/Base/BaseButton.vue";
</script>
<template>
  <div
    class="bg-indigo-600 py-12 px-20 text-white sm:rounded-md md:py-20 lg:py-32"
  >
    <div class="text-4xl font-extrabold">
      <slot name="title"
        >Boost your productivity.<br />Start using Awsme today.</slot
      >
    </div>
    <div class="mx-auto mt-4 max-w-xl text-slate-200">
      <slot name="text">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quo, cum,
        quidem vitae eius hic animi nihil sequi nostrum exercitationem rem
        corporis nemo optio distinctio tempora quis blanditiis alias impedit
        cupiditate.
      </slot>
    </div>
    <BaseButton class="my-10" :customStyle="'bg-slate-100 text-indigo-800'"
      ><slot>Sign up for free</slot></BaseButton
    >
  </div>
</template>
