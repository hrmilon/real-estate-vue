<script setup lang="ts">
import { Card, CardContent } from '@/components/ui/card'
import { Carousel, CarouselContent, CarouselItem, CarouselNext, CarouselPrevious } from '@/components/ui/carousel'

const carouselItem = [
    {
        text: 'Free Sold',
        image: 'https://ap.rdcpix.com/9b9b2029a7b41aff2ac78f1438e042b6l-m4108336929rd-w480_h360.webp',
        url: 'products/1'
    },
    {
        text: 'Modern Villa',
        image: 'https://ap.rdcpix.com/9b9b2029a7b41aff2ac78f1438e042b6l-m4108336929rd-w480_h360.webp',
        url: 'products/2'
    },
    {
        text: 'Luxury Apartment',
        image: 'https://ap.rdcpix.com/9b9b2029a7b41aff2ac78f1438e042b6l-m4108336929rd-w480_h360.webp',
        url: 'products/3'
    },
    {
        text: 'Cozy Cottage',
        image: 'https://ap.rdcpix.com/9b9b2029a7b41aff2ac78f1438e042b6l-m4108336929rd-w480_h360.webp',
        url: 'products/4'
    },
    {
        text: 'Beachfront Property',
        image: 'https://ap.rdcpix.com/9b9b2029a7b41aff2ac78f1438e042b6l-m4108336929rd-w480_h360.webp',
        url: 'products/5'
    }
];


</script>

<template>
    <div class="container mx-auto py-10 px-4">

        <div class="font-medium text-2xl mb-4">
            Browse homes in Austin, TX
        </div>

        <Carousel class="w-full max-w-5xl mx-auto" :opts="{
            align: 'center',
        }">
            <CarouselContent>
                <CarouselItem v-for="item in carouselItem" :key="item.text" class="md:basis-1/2 lg:basis-1/3 pl-4 pr-4">
                    <RouterLink :to="item.url">
                        <Card class="border-2 shadow-md">
                            <CardContent class="flex items-center justify-center p-0 min-h-[200px] relative">
                                <span class="inset-3 absolute text-sm text-black/50 font-bold">{{ item.text }}</span>
                                <img class="brightness-80" :src="item.image" alt="">
                            </CardContent>
                        </Card>
                    </RouterLink>
                </CarouselItem>
            </CarouselContent>
            <div class="flex justify-center gap-4 mt-10">
                <CarouselPrevious class="relative static" />
                <CarouselNext class="relative static" />
            </div>
        </Carousel>
    </div>
</template>
