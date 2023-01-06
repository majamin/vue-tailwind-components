<script setup lang="ts">
import BaseIcon from '@/components/Base/BaseIcon.vue'
</script>
<template>
  <div class="py-24 sm:py-32 lg:py-40">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="sm:text-center">
        <h2 class="text-lg font-serif font-semibold leading-8 text-indigo-600">
          <slot name="title"></slot>
        </h2>
        <p
          class="mt-2 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl"
        >
          <slot name="tagline">2x2 Grid</slot>
        </p>
        <p class="mx-auto mt-6 max-w-2xl text-lg leading-8 text-gray-600">
          <slot name="tagline-more">
            Lorem ipsum dolor sit amet consect adipisicing elit. Possimus magnam
            voluptatum cupiditate veritatis in accusamus quisquam.
          </slot>
        </p>
      </div>

      <div class="mt-20 max-w-lg sm:mx-auto md:max-w-none">
        <div
          class="grid grid-cols-1 gap-y-16 md:grid-cols-2 md:gap-x-12 md:gap-y-16"
        >
          <!-- ▒▒▒▒▒▒▒▒▒TOP LEFT▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒ -->
          <div
            class="relative flex flex-col text-left gap-6 sm:flex-row md:flex-col lg:flex-row"
          >
            <BaseIcon>supervised_user_circle</BaseIcon>
            <div class="sm:min-w-0 sm:flex-1">
              <p class="text-lg font-semibold leading-8 text-gray-900">
                <slot name="top-left-heading">Top left heading</slot>
              </p>
              <p class="mt-2 text-base leading-7 text-gray-600">
                <slot name="top-left-text">
                  Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                  Maiores impedit perferendis suscipit eaque, iste dolor
                  cupiditate blanditiis ratione.
                </slot>
              </p>
            </div>
          </div>
          <!-- ▒▒▒▒▒▒▒▒▒TOP RIGHT▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒ -->
          <div
            class="relative flex flex-col text-left gap-6 sm:flex-row md:flex-col lg:flex-row"
          >
            <BaseIcon>face</BaseIcon>
            <div class="sm:min-w-0 sm:flex-1">
              <p class="text-lg font-semibold leading-8 text-gray-900">
                <slot name="top-left-heading">Top right heading</slot>
              </p>
              <p class="mt-2 text-base leading-7 text-gray-600">
                <slot name="top-left-text">
                  Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                  Maiores impedit perferendis suscipit eaque, iste dolor
                  cupiditate blanditiis ratione.
                </slot>
              </p>
            </div>
          </div>
          <!-- ▒▒▒▒▒▒▒▒▒BOTTOM LEFT▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒ -->
          <div
            class="relative flex flex-col text-left gap-6 sm:flex-row md:flex-col lg:flex-row"
          >
            <BaseIcon>assessment</BaseIcon>
            <div class="sm:min-w-0 sm:flex-1">
              <p class="text-lg font-semibold leading-8 text-gray-900">
                <slot name="top-left-heading">Bottom left heading</slot>
              </p>
              <p class="mt-2 text-base leading-7 text-gray-600">
                <slot name="top-left-text">
                  Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                  Maiores impedit perferendis suscipit eaque, iste dolor
                  cupiditate blanditiis ratione.
                </slot>
              </p>
            </div>
          </div>
          <!-- ▒▒▒▒▒▒▒▒▒BOTTOM RIGHT▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒ -->
          <div
            class="relative flex flex-col text-left gap-6 sm:flex-row md:flex-col lg:flex-row"
          >
            <BaseIcon>receipt</BaseIcon>
            <div class="sm:min-w-0 sm:flex-1">
              <p class="text-lg font-semibold leading-8 text-gray-900">
                <slot name="top-left-heading">Bottom right heading</slot>
              </p>
              <p class="mt-2 text-base leading-7 text-gray-600">
                <slot name="top-left-text">
                  Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                  Maiores impedit perferendis suscipit eaque, iste dolor
                  cupiditate blanditiis ratione.
                </slot>
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
