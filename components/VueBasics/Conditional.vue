<script setup lang="ts">
import { ref } from "vue";
import BaseButton from "@/components/Base/BaseButton.vue";
const toggled = ref(true);
</script>
<template>
  <div>
    <BaseButton @click="toggled = !toggled">Toggle</BaseButton>
    <h2 v-if="toggled">Vue is awesome!</h2>
    <h2 v-else>Oh no 😢</h2>
  </div>
</template>
