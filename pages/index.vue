<script setup lang="ts">
import MountainCarousel from '@/components/montpic/MountainCarousel.vue'
import { APP_NAME, APP_SLOGAN } from '@/constants/config'
</script>

<template>
    <div class="flex flex-col items-center justify-start text-center min-h-screen p-2 pt-10 gap-4">
        <h1 class="text-6xl lg:text-9xl font-bold">{{ APP_NAME }}</h1>
        <p class="text-2xl">{{ APP_SLOGAN }}</p>
    </div>
    <NuxtImg src="/mountain.webp" class="fixed w-screen -z-50 align-middle -bottom-1/12 sm:-bottom-1/5 md:-bottom-1/4 lg:-bottom-1/3 xl:-bottom-2/5 blur-sm brightness-75 dark:brightness-100" />
</template>