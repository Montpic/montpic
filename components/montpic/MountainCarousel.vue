<script setup lang="ts">
import { Card, CardContent } from '@/components/ui/card'
import { Carousel, CarouselContent, CarouselItem, CarouselNext, CarouselPrevious } from '@/components/ui/carousel'

const images = [
    { name: 'Montagne du roule', link: '/roule.webp' },
    { name: 'Montagne du roule', link: '/roule.webp' },
    { name: 'Montagne du roule', link: '/roule.webp' },
    { name: 'Montagne du roule', link: '/roule.webp' },
    { name: 'Montagne du roule', link: '/roule.webp' },
]
</script>

<template>
    <Carousel v-slot="{ canScrollNext }" class="relative w-full max-w-xs md:max-w-md">
        <CarouselContent>
            <CarouselItem v-for="(image, index) in images" :key="index">
                <div class="p-1">
                    <Card>
                        <CardContent class="flex flex-col aspect-square items-center justify-center p-6">
                            <img :src="image.link" />
                            <p>{{ image.name }}</p>
                        </CardContent>
                    </Card>
                </div>
            </CarouselItem>
        </CarouselContent>
        <CarouselPrevious />
        <CarouselNext v-if="canScrollNext" />
    </Carousel>
</template>

<script lang="ts">
export default {
    name: 'MountainCarousel',
}
</script>