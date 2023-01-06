<!-----------------------------------------------------------------------------
▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒
▒                                                                             ▒
▒   ~ Computed properties ~                                                   ▒
▒   Computed properties are cached and only update when their                 ▒
▒   dependencies change. Regular methods have no such guarantees.             ▒
▒   https://vuejs.org/guide/essentials/reactivity-fundamentals.html           ▒
▒                                                                             ▒
▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒
------------------------------------------------------------------------------>
<script setup lang="ts">
import { computed, ref } from "vue";

const upperFood = computed(() => {
  return food.value?.toUpperCase();
});

const food = ref<string | null>();
</script>

<template>
  <div>
    <div class="flex items-center justify-center align-middle">
      <div class="mr-6">What's your favourite food?</div>
      <div class="w-fit">
        <input
          v-model="food"
          placeholder="Type here"
          class="border-box w-full border-0 bg-white p-4 text-base text-slate-500 outline-none"
        />
      </div>
    </div>
    <div class="mt-6 flex h-20 flex-col bg-blue-100">
      <div class="my-auto" v-if="food">Yum, yum, {{ upperFood }}!</div>
      <div class="my-auto" v-else>Yum, yum!</div>
    </div>
  </div>
</template>
