<script setup lang="ts">
import Navigation from '@/components/custom/Navigation.vue';
import { Button } from "@/components/ui/button"

</script>

<template>
    <div class="flex justify-between items-center mx-5 py-3">
        <div class="">
            <img class="w-16" src="/assets/real-estate-logo.png" alt="">
        </div>
        <Navigation class=""/>
        <div class="space-x-4">
            <Button class="rounded-full" variant="outline">Login</Button>
            <Button class="rounded-full">Sign Up</Button>
        </div>
    </div>
</template>