<script setup lang="ts">
import { ref } from 'vue'
import { faker } from '@faker-js/faker'

const currentTheme = ref('cupcake')

const randomTheme = () => {
  currentTheme.value = faker.helpers.arrayElement(['cupcake', 'dark', 'cmyk', 'cyberpunk', 'synthwave'])
  return currentTheme
}
</script>

<template>
  <div :data-theme="currentTheme" class="flex flex-col">
    <div class="tabs">
      <a class="tab">Tab 1</a>
      <a class="tab tab-active">Tab 2</a>
      <a class="tab">Tab 3</a>
    </div>
    <button class="btn btn-primary" @click="randomTheme()">
      Current theme: {{ currentTheme }}
    </button>

    <div v-for="i in 6" :key="i" class="flex flex-row justify-between">
      <div class="card w-96 bg-base-100 shadow-xl m-4">
        <figure><img :src="faker.image.animals()" alt="Shoes"></figure>
        <div class="card-body">
          <h2 class="card-title">
            Shoes!
          </h2>
          <p>If a dog chews shoes whose shoes does he choose?</p>
          <div class="card-actions justify-end">
            <button class="btn btn-primary">
              Buy Now
            </button>
          </div>
        </div>
      </div>
    </div>
    <div class="alert shadow-lg">
      <div>
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" class="stroke-info flex-shrink-0 w-6 h-6"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 16h-1v-4h-1m1-4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z" /></svg>
        <span>we use cookies for no reason.</span>
      </div>
      <div class="flex-none">
        <button class="btn btn-sm btn-ghost">
          Deny
        </button>
        <button class="btn btn-sm btn-primary">
          Accept
        </button>
      </div>
    </div>
    <div class="grid grid-flow-col gap-5 text-center auto-cols-max">
      <div class="flex flex-col p-2 bg-neutral rounded-box text-neutral-content">
        <span class="countdown font-mono text-5xl">
          <span style="--value:15;" />
        </span>
        days
      </div>
      <div class="flex flex-col p-2 bg-neutral rounded-box text-neutral-content">
        <span class="countdown font-mono text-5xl">
          <span style="--value:10;" />
        </span>
        hours
      </div>
      <div class="flex flex-col p-2 bg-neutral rounded-box text-neutral-content">
        <span class="countdown font-mono text-5xl">
          <span style="--value:24;" />
        </span>
        min
      </div>
      <div class="flex flex-col p-2 bg-neutral rounded-box text-neutral-content">
        <span class="countdown font-mono text-5xl">
          <span style="" />
        </span>
        sec
      </div>
    </div>
    <div class="flex justify-center gap-1 my-1 w-full">
      <kbd class="kbd">q</kbd>
      <kbd class="kbd">w</kbd>
      <kbd class="kbd">e</kbd>
      <kbd class="kbd">r</kbd>
      <kbd class="kbd">t</kbd>
      <kbd class="kbd">y</kbd>
      <kbd class="kbd">u</kbd>
      <kbd class="kbd">i</kbd>
      <kbd class="kbd">o</kbd>
      <kbd class="kbd">p</kbd>
    </div>
    <div class="flex justify-center gap-1 my-1 w-full">
      <kbd class="kbd">a</kbd>
      <kbd class="kbd">s</kbd>
      <kbd class="kbd">d</kbd>
      <kbd class="kbd">f</kbd>
      <kbd class="kbd">g</kbd>
      <kbd class="kbd">h</kbd>
      <kbd class="kbd">j</kbd>
      <kbd class="kbd">k</kbd>
      <kbd class="kbd">l</kbd>
    </div>
    <div class="flex justify-center gap-1 my-1 w-full">
      <kbd class="kbd">z</kbd>
      <kbd class="kbd">x</kbd>
      <kbd class="kbd">c</kbd>
      <kbd class="kbd">v</kbd>
      <kbd class="kbd">b</kbd>
      <kbd class="kbd">n</kbd>
      <kbd class="kbd">m</kbd>
      <kbd class="kbd">/</kbd>
    </div>
  </div>
</template>
