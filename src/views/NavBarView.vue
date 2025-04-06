<script setup lang="ts">
import Navigation from '@/components/custom/Navigation.vue';
import { Button } from "@/components/ui/button"
import { CircleX, Menu } from 'lucide-vue-next';
import { ref } from 'vue';
import {
    Card,
    CardContent,
    CardDescription,
    CardFooter,
    CardHeader,
    CardTitle,
} from "@/components/ui/card"

const navlinkMobile = [
    {
        name: 'Sell',
        href: '#'
    },
    {
        name: 'Buy',
        href: '#'
    },
    {
        name: 'Rent',
        href: '#'
    },
    {
        name: 'Advertise',
        href: '#'
    },
    {
        name: 'Contact Us',
        href: '#'
    }

]


const isOpen = ref(false);
const toggleMenu = () => (isOpen.value = !isOpen.value);
</script>

<template>
    <div class="flex justify-between items-center mx-5 py-3">
        <div class="">
            <img class="w-16" src="/assets/real-estate-logo.png" alt="">
        </div>
        <Navigation class="hidden sm:block" />
        <div class="flex justify-center items-center space-x-4">
            <Button class="rounded-full" variant="outline">Login</Button>
            <Button class="rounded-full">Sign Up</Button>
            <Menu @click="toggleMenu" class="block md:hidden" />
        </div>
    </div>

    <div v-if="isOpen" class="w-full top-0 z-50 relative">
        <Card class="w-2/3 absolute right-0 rounded-sm">
            <CardHeader>
                <Button class="w-2 rounded-sm" @click="isOpen = false">
                    <CircleX />
                </Button>
            </CardHeader>
            <CardContent class="flex flex-col space-y-2">
                <RouterLink class="hover:bg-gray-800/10 p-2 rounded-sm" v-for="link of navlinkMobile"
                    v-bind:key="link.href" to="#">{{ link.name }}</RouterLink>
            </CardContent>
            <CardFooter>

            </CardFooter>
        </Card>
    </div>

</template>