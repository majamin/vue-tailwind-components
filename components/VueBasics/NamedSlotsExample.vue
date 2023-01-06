<template>
  <div>
    <div class="flex flex-wrap justify-center gap-10 text-center align-middle">
      <div class="flex max-w-fit">
        <div
          class="tilt-square bg-amber-500 text-amber-800"
        >
          <slot name="left"></slot>
        </div>
      </div>
      <div class="flex max-w-fit">
        <div
          class="tilt-square bg-cyan-500 text-cyan-800"
        >
          <slot name="middle"></slot>
        </div>
      </div>
      <div class="flex max-w-fit">
        <div
          class="tilt-square bg-fuchsia-500 text-fuchsia-800"
        >
          <slot name="right"></slot>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="postcss">
.tilt-square {
  @apply h-36 w-36 pt-4 text-xl font-black transition-all duration-500 ease-in-expo hover:rotate-6;
}
</style>
