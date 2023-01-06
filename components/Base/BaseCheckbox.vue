<script setup lang="ts">
import UniqueID from "@/features/UniqueID";

const uuid = UniqueID().getID().toString();

const emit = defineEmits<{
  (e: 'update:modelValue', checked: boolean): void
}>()

defineProps({
  label: {
    type: String,
    default: "",
  },
  modelValue: {
    type: Boolean,
    default: false,
  },
});
</script>
<template>
  <div class="flex">
    <div class="mr-4">
      <input
        :checked="modelValue"
        :id="uuid"
        type="checkbox"
        @change="
        emit(
          'update:modelValue',
          ($event.target as HTMLInputElement).checked
        )
        "
        class="border-box text-slate-500 w-full rounded-md border-2 p-4 text-base outline-none"
      />
    </div>
    <div>
      <label
        :for="uuid"
      >{{ label }}</label
      >
    </div>
  </div>
  <!-- <p class="h-1.5 text-xs text-theme-red-500"> -->
  <!--   {{ error }} -->
  <!-- </p> -->
</template>
