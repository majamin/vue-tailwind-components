<!-----------------------------------------------------------------------------
▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒
▒                                                                             ▒
▒   ~ Class and Style Bindings ~                                              ▒
▒   Vue adds enhancements to the v-bind directive so classes and styles       ▒
▒   can be added and removed in the component logic.                          ▒
▒   https://vuejs.org/guide/essentials/class-and-style.html                   ▒
▒                                                                             ▒
▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒
------------------------------------------------------------------------------>
<script setup lang="ts">
import { computed, ref } from "vue";

const email = ref<string | null>();
const age = ref();

// NOTE: This is just an example.
// In practice, it is better to use a library like VeeValidate
const isValidEmail = computed(() => {
  return (
    String(email.value)
      .toLowerCase()
      .match(
        /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/
      ) !== null
  );
});

const isValidAge = computed(() => {
  const parsed = parseInt(age.value);
  return (!isNaN(parsed)) && (typeof parsed === "number");
});

</script>

<template>
  <div>
    <input
      v-model="email"
      placeholder="Test your email address here"
      class="w-full border-2 bg-white p-4 text-base text-slate-500 outline-none"
      :class="isValidEmail ? 'border-green-300' : 'border-red-300'"
    />
    <input
      v-model="age"
      placeholder="Enter your age"
      class="mt-4 w-full border-2 bg-white p-4 text-base text-slate-500 outline-none"
      :class="isValidAge ? 'border-green-300' : 'border-red-300'"
    />
  </div>
</template>
