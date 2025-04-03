<script setup>
import { RouterLink } from 'vue-router';
import { Input } from "@/components/ui/input"
import { Search } from 'lucide-vue-next';
import Button from '../ui/button/Button.vue';

</script>

<template>
    <div class="relative bg-[url(/assets/realtor-hero.jpg)] bg-no-repeat bg-cover bg-center  h-[450px] w-full flex flex-col items-center justify-center space-y-6">
        <div class="text-white text-6xl max-w-xl text-center font-serif">
            The #1 site real estate professionals trust*
        </div>

        <div class="relative flex flex-row items-center justify-center">
            <Input placeholder="Address, School, City, Zip or Neighborhood" class="bg-white w-[500px] rounded-full h-[50px]" />
            <Button class="absolute right-1 w-10 h-10 rounded-full">
                <Search />
            </Button>

        </div>

    </div>
</template>