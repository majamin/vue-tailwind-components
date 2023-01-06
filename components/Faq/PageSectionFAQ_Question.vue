<script setup lang="ts">
import { ref } from "vue";
const toggled = ref(false);
</script>
<template>
  <div
    @click="toggled = !toggled"
    class="flex cursor-pointer bg-indigo-100 flex-col space-y-8 rounded-md px-8 text-left py-8 shadow-md shadow-gray-400"
  >
    <div class="flex space-x-6">
      <div class="flex w-full flex-col">
        <div class="flex">
          <div class="mr-2 text-xl font-black text-indigo-700">
            <slot name="prompt">
              What important event took place on December 16, 1773?
            </slot>
          </div>
          <div class="flex flex-col justify-center">
            <span
              :class="toggled ? '-rotate-270' : '-rotate-90'"
              class="material-icons md-48 font-black text-gray-500 transition-all duration-300"
              >expand_more</span
            >
          </div>
        </div>
        <Transition name="slide-fade"
          ><div v-if="toggled" class="mt-4 font-light">
            <slot name="answer"
              >I do not believe in linear time. There is no past and future: all
              is one, and existence in the temporal sense is illusory. This
              question, therefore, is meaningless and impossible to
              answer.</slot
            >
          </div></Transition
        >
      </div>
    </div>
  </div>
</template>

<style lang="postcss">
.slide-fade-enter-active {
  @apply transition-all duration-300 ease-out;
}
.slide-fade-leave-active {
  @apply transition-all duration-300;
}
.slide-fade-enter-from,
.slide-fade-leave-to {
  @apply -translate-y-5 opacity-0;
}
</style>
