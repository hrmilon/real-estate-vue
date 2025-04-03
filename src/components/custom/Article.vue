<script setup lang="ts">
import Button from '../ui/button/Button.vue';

</script>

<template>
    <div
        class="bg-[url(/assets/article-img.jpg)] w-full h-[300px] bg-cover bg-center flex items-center justify-center flex-col gap-y-4 brightness-75">
        <!-- title -->
        <div class="text-white font-bold text-lg filter-none">
            Unique Homes
        </div>

        <!-- content -->
        <div class="font-extrabold text-white max-w-lg text-center text-xl">
            $79 Million Aspen Megamansion With Wild Array of Amenities Including Indoor Pool and 4 Bars Is the Week’s
            Most Expensive Home
        </div>

        <!-- button -->

        <div>
            <Button variant="outline" class="rounded-full">Read Article</Button>
        </div>
    </div>
</template>