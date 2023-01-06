<script setup lang="ts">
import Question from "@/components/Faq/PageSectionFAQ_Question.vue";
const { dark } = defineProps<{ dark: false }>();
</script>
<template>
  <div class="flex flex-col space-y-8">
    <Question>
      <template v-slot:prompt>Why Is the Sky Blue?</template>
      <template v-slot:answer
        >Blue light waves travel in short, choppy waves. Like each of the other
        colours, blue light waves are scattered and reflected as they enter
        Earth's atmosphere and collide with gases and other particles. Because
        the colour blue has the shortest wavelength, it collides with nearly
        everything in its path and is scattered about the sky. This is why the
        sky appears blue.</template
      >
    </Question>
    <Question>
      <template v-slot:prompt>Is the Sky Blue Because of the Ocean?</template>
      <template v-slot:answer
        >No, the sky is blue because blue light waves have a short wavelength,
        causing this colour to get caught in the sky as it collides with gases
        and other particles.</template
      >
    </Question>
    <Question>
      <template v-slot:prompt>Why Is the Sunset Red or Orange?</template>
      <template v-slot:answer
        >When the sun is setting, the light that reaches you has had to go
        through lots more atmosphere than when the sun is overhead, hence the
        only colour light that is not scattered away is the long wavelength
        light, the red.</template
      >
    </Question>
  </div>
</template>
