<script setup lang="ts">
type Props = {
  y: number;
  goTop: () => void;
};

const { y, goTop } = defineProps<Props>();

const isOpen = ref(false);

import { NAV_LINKS } from "@/data/constants";
</script>

<template>
  <header
    class="sticky z-20 top-0 duration-200 px-4 border-b border-solid"
    :class="{
      'py-4 dark:bg-black bg-slate-200 border-primary border-b-2': y > 0,
      'py-6 bg-transparent border-transparent': y <= 0,
    }"
  >
    <nav class="flex flex-row items-center justify-between max-w-[1400px] mx-auto">
      <div class="flex gap-4 items-center cursor-pointer text-primary hover:text-blue-300" @click="goTop">
        <span class="inline-block">
          <img src="/kotonelogo.png" alt="Kotone Logo" class="h-6 w-6" />
        </span>
        <h1 class="font-medium text-xl">
          <b class="font-bold poppins mr-1">KangJono</b>
        </h1>
      </div>

      <div class="flex gap-4 items-center ml-auto relative" v-motion-fade-visible-once>
        <ThemeToggler />
        <button
          aria-label="expand mobile menu button"
          @click="isOpen = !isOpen"
          class="md:hidden block p-2 absolute top-0 right-0"
          :class="{
            open: isOpen,
            'focus:outline-none': true,
          }"
        >
          <span class="hamburger-top"></span>
          <span class="hamburger-middle"></span>
          <span class="hamburger-bottom"></span>
        </button>
      </div>

      <nav class="items-center flex-row hidden md:flex">
        <div class="flex pr-3">
          <div class="sm:flex items-center gap-4 text-center hidden">
            <a class="hover:text-primary hover:underline" v-for="link in NAV_LINKS" :href="link.href" :key="link.href">{{ link.label }} </a>
          </div>
        </div>
        <div class="flex gap-4">
          <a href="https://github.com/" target="_blank">
            <svg class="h-6 w-6 text-black dark:text-white" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
              <path
                fill-rule="evenodd"
                d="M12 2C6.477 2 2 6.477 2 12c0 4.418 2.865 8.166 6.839 9.489.5.09.682-.217.682-.482 0-.237-.009-.868-.014-1.703-2.782.604-3.369-1.34-3.369-1.34-.454-1.155-1.11-1.462-1.11-1.462-.908-.62.069-.607.069-.607 1.004.071 1.533 1.032 1.533 1.032.892 1.53 2.341 1.087 2.91.832.091-.647.35-1.086.636-1.335-2.22-.252-4.555-1.11-4.555-4.943 0-1.091.39-1.984 1.029-2.683-.103-.253-.446-1.27.098-2.646 0 0 .84-.269 2.75 1.025A9.564 9.564 0 0112 6.845c.853.004 1.71.115 2.512.337 1.907-1.294 2.746-1.025 2.746-1.025.547 1.376.204 2.393.1 2.646.64.699 1.027 1.592 1.027 2.683 0 3.842-2.338 4.687-4.566 4.934.36.31.68.918.68 1.851 0 1.335-.012 2.415-.012 2.741 0 .268.18.576.688.479A10.017 10.017 0 0022 12c0-5.523-4.477-10-10-10z"
                clip-rule="evenodd"
              />
            </svg>
          </a>
        </div>
      </nav>
    </nav>

    <nav
      v-show="isOpen"
      @click="isOpen = false"
      class="md:hidden p-4 mt-2 flex flex-col gap-2 text-center font-bold"
      :class="{
        'py-4 dark:bg-slate-950 bg-slate-200 border-primary dark:border-green-950': y > 0,
        'py-6 bg-transparent border-transparent': y <= 0,
      }"
    >
      <a class="border rounded p-2 border-primary animate-link" v-for="link in NAV_LINKS" :href="link.href" :key="link.href">{{ link.label }} </a>
      <div class="flex gap-4 justify-center">
        <a href="https://github.com/" target="_blank">
          <svg class="h-6 w-6 text-black dark:text-white" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
            <path
              fill-rule="evenodd"
              d="M12 2C6.477 2 2 6.477 2 12c0 4.418 2.865 8.166 6.839 9.489.5.09.682-.217.682-.482 0-.237-.009-.868-.014-1.703-2.782.604-3.369-1.34-3.369-1.34-.454-1.155-1.11-1.462-1.11-1.462-.908-.62.069-.607.069-.607 1.004.071 1.533 1.032 1.533 1.032.892 1.53 2.341 1.087 2.91.832.091-.647.35-1.086.636-1.335-2.22-.252-4.555-1.11-4.555-4.943 0-1.091.39-1.984 1.029-2.683-.103-.253-.446-1.27.098-2.646 0 0 .84-.269 2.75 1.025A9.564 9.564 0 0112 6.845c.853.004 1.71.115 2.512.337 1.907-1.294 2.746-1.025 2.746-1.025.547 1.376.204 2.393.1 2.646.64.699 1.027 1.592 1.027 2.683 0 3.842-2.338 4.687-4.566 4.934.36.31.68.918.68 1.851 0 1.335-.012 2.415-.012 2.741 0 .268.18.576.688.479A10.017 10.017 0 0022 12c0-5.523-4.477-10-10-10z"
              clip-rule="evenodd"
            />
          </svg>
        </a>
      </div>
    </nav>
  </header>
</template>
