<script setup>
import { Button } from "@/components/ui/button"
import { Input } from "@/components/ui/input"
import { Search } from "lucide-vue-next";
</script>
<template>
    <div class="hidden md:block">
        <div class="flex mt-10">
            <div class="w-1/2">
                <img class="bg-center" src="/assets/desktop-boy.jpg" alt="">
            </div>
            <div class="w-1/2 flex flex-col justify-center items-start p-10 space-y-5">
                <div class="text-2xl font-bold">Need a home loan? Get pre-approved</div>
                <div>Find a lender who can offer competitive mortgage rates and help you with pre-approval.</div>
                <div>
                    <Button class="rounded-full">Get Pre Approved Now</Button>
                </div>
            </div>
        </div>

        <div class="flex">
            <div class="w-1/2 flex flex-col justify-center items-start p-10 space-y-5">
                <div class="text-2xl font-bold">Get Local Info</div>
                <div>Does it have pet-friendly rentals? How are the schools? Get important local information on the area
                    you're most interested in.</div>
                <div>
                    <!-- <Button>Button</Button> -->
                    <div class="relative flex flex-row items-center justify-center">
                        <Input placeholder="San Francisko" class="bg-white w-[400px] rounded-full h-[50px]" />
                        <Button class="absolute right-1 w-10 h-10 rounded-full">
                            <Search />
                        </Button>

                    </div>
                </div>
            </div>
            <div class="w-1/2">
                <img src="/assets/desktop-boy.jpg" alt="">
            </div>
        </div>

    </div>
</template>