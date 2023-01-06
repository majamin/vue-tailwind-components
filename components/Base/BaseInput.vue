<script setup lang="ts">
import { ref } from "vue";
import UniqueID from "@/features/UniqueID";

const uuid = UniqueID().getID().toString();
const focused = ref(false);

defineEmits(["update:modelValue"]);
defineProps({
  label: {
    type: String,
    default: "",
  },
  placeholder: { type: String, default: "" },
  type: {
    type: String,
    default: "text",
  },
  modelValue: {
    type: [String, Number],
    default: "",
  },
  error: {
    type: String,
    default: "",
  },
});
</script>
<template>
  <label
    :for="uuid"
    class="mb-2 text-sm font-medium transition-opacity duration-500 ease-in-out"
    :class="{
      'text-red-600': error,
      'text-gray-600': !error,
    }"
    >{{ error ? error : label }}</label
  >
  <input
    v-bind="$attrs"
    :value="modelValue"
    :placeholder="placeholder"
    :id="uuid"
    :type="type"
    @input="
      $emit('update:modelValue', ($event.target as HTMLInputElement).value)
    "
    @focusin="focused = true"
    @focusout="focused = false"
    class="border-box text-slate-500 w-full rounded-md border-2 p-4 text-base outline-none"
    :class="focused ? 'border-pastel-blue' : ''"
  />
  <!-- <p class="h-1.5 text-xs text-theme-red-500"> -->
  <!--   {{ error }} -->
  <!-- </p> -->
</template>
