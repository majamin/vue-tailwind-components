<!-----------------------------------------------------------------------------
▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒
▒                                                                             ▒
▒                                                                             ▒
▒                                                                             ▒
▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒
------------------------------------------------------------------------------>

<script setup lang="ts">
import BaseButton from "@/components/Base/BaseButton.vue";
</script>
<template>
  <div class="flex flex-col overflow-hidden md:flex-row">
    <div class="flex items-center justify-center overflow-hidden md:w-4/5">
      <img class="h-full w-full object-cover" src="meeting.jpg" alt="" />
    </div>
    <div
      class="flex w-full flex-col items-center justify-center bg-indigo-600 p-10 text-white md:w-4/5"
    >
      <div class="my-6 text-4xl font-extrabold leading-relaxed">
        <slot name="title"
          >Boost your productivity.<br />Start using Awsme today.</slot
        >
      </div>
      <div class="mx-auto my-6 max-w-xl text-slate-200">
        <slot name="text">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Quo, cum,
          quidem vitae eius hic animi nihil sequi nostrum exercitationem rem
          corporis nemo optio distinctio tempora quis blanditiis alias impedit
          cupiditate.
        </slot>
      </div>
      <BaseButton class="my-6" :customStyle="'bg-slate-100 text-indigo-800'"
        ><slot>Sign up for free</slot></BaseButton
      >
    </div>
  </div>
</template>
