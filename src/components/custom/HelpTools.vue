<script setup>
import { Button } from "@/components/ui/button"
import {
    Card,
    CardContent,
    CardDescription,
    CardFooter,
    CardHeader,
    CardTitle,
} from "@/components/ui/card"
import { SquareMousePointer } from "lucide-vue-next";

const helps = [
    {
        title: 'Find out how much you can afford',
        text: 'Well help you estimate your budget range. Save to your buyer profile to help in your search.',
        action: 'Try our affordability calculator'
    },
    {
        title: 'Find out how much you can afford',
        text: 'Well help you estimate your budget range. Save to your buyer profile to help in your search.',
        action: 'Try our affordability calculator'
    },
    {
        title: 'Find out how much you can afford',
        text: 'Well help you estimate your budget range. Save to your buyer profile to help in your search.',
        action: 'Try our affordability calculator'
    },
]


</script>
<template>
    <div class="p-10">
        <!-- titel -->
        <div class="text-lg font-bold my-3">
            Discover how we can help
        </div>

        <!-- button -->
        <div class="my-3">
            <ul class="list-none">
                <li class="inline mr-1"><Button class="rounded-full">Buying</Button></li>
                <li class="inline mr-1"><Button variant="outline" class="rounded-full">Renting</Button></li>
                <li class="inline "><Button variant="outline" class="rounded-full">Selling</Button></li>
            </ul>
        </div>

        <!-- card -->
        <div class="flex flex-row justify-center gap-2">
            <Card v-for="help in helps" v-bind:key="help" class="w-[400px] h-[200px]">
                <CardHeader>
                    <div class="flex justify-between">
                        <div>
                            <CardTitle>{{ help.title }}</CardTitle>
                        </div>
                        <div>
                            <SquareMousePointer />
                        </div>
                    </div>

                </CardHeader>
                <CardContent>
                    {{ help.text }}
                </CardContent>
                <CardFooter>
                    <p class="text-sm">
                        <RouterLink class="underline" to="/" >{{ help.action }}</RouterLink> 
                    </p>
                </CardFooter>
            </Card>
        </div>
    </div>
</template>