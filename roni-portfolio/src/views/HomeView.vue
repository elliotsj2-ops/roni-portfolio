<script setup lang="ts">
import coverImage from '@/assets/cover-photo.jpg'
import backgroundImage from '@/assets/redwoods.jpg'
import { ref } from 'vue'

const services = ref([
    {
        title: "Regenerative Teaching Circles",
        description: "We grow in community. Teaching Circles offer a place for connection, learning, heartfelt sharing and encouragement... because teaching can be isolating, and we don’t have to hold our challenges alone."
    },
    {
        title: "Regenerative Teaching 1:1 Coaching",
        description: "Through personalized coaching, I listen with compassion and connect you with new tools – so you have the capacity to respond with more presence and attunement."
    },
    {
        title: "Regenerative Teaching Workshops",
        description: "Customized workshops that provide tangible take-aways on how to create restorative classrooms and teams…starting tomorrow! Topics include:",
        list: [
            "Restorative Teaching 101",
            "Restorative Communication: Keys to Supporting Accountability",
            "Responding to Conflict with Care",
            "Fostering Constructive Discourse in the Classroom",
            "Circling Up to Build Belonging"
        ]
    }
]);

const googleFormLink = "https://docs.google.com/forms/d/e/1FAIpQLScRzleZT_WzMKyhF3texyEzzQadUwPUTvAhvUha2Znny0j_Fw/viewform"
</script>

<template>
    <div class="relative bg-cover bg-center bg-no-repeat" :style="{ backgroundImage: `url(${backgroundImage})` }">
        <div class="absolute inset-0 bg-black/50 backdrop-blur-sm"></div>
        <div class="relative z-10 flex flex-col items-center justify-center gap-8 font-montserrat pt-16 bg-[rgb(220,220,230,0.6)]">
            <div class="flex flex-row">
                <div class="flex flex-col gap-4 w-2/3 p-8 items-start justify-center">
                    <h1 class="text-5xl font-bold text-gray-800">Hi, I'm Roni Ben-David</h1>
                    <p class="text-lg text-gray-700">
                        I founded Regenerative Teaching Consulting to support schools in authentically deepening their inclusion work, by building the skills and capacity of their teachers.
                    </p>
                    <p class="text-lg text-gray-700">
                        My approach is to offer warm, practical guidance, grounded in restorative and trauma-based approaches to teaching. 
                    </p>

                    <v-btn variant="outlined" rounded="xl" size="large" append-icon="mdi-arrow-right" :href="googleFormLink" target="_blank" color="#006622" class="!bg-[rgba(0,102,34,0.1)]">
                        Get In Touch
                    </v-btn>
                </div>
                <div class="w-1/3 h-auto relative">
                    <img :src="coverImage" alt="Cover Photo" class="w-full h-full object-cover [mask-image:linear-gradient(to_left,rgba(0,0,0,1)_0%,rgba(0,0,0,1)_70%,rgba(0,0,0,0)_100%)] [-webkit-mask-image:linear-gradient(to_left,rgba(0,0,0,1)_0%,rgba(0,0,0,1)_70%,rgba(0,0,0,0)_100%)]" />
                </div>
            </div>

            <div class="flex flex-col items-center justify-center w-full px-12">
                <div class="flex flex-row items-center justify-center w-full">
                    <div class="flex-grow border-t border-black"></div>
                    <span class="text-4xl font-semibold text-black py-8 px-12">
                        Services
                    </span>
                    <div class="flex-grow border-t border-black"></div>
                </div>
                
                <div class="flex flex-col md:flex-row gap-8 py-8">
                    <div v-for="(service, index) in services" :key="index" class="flex flex-col gap-4 p-8 bg-[rgb(220,220,230,0.6)] rounded-lg shadow-md">
                        <h2 class="text-center font-italic text-xl font-bold text-gray-800">
                            {{ service.title }}
                        </h2>
                        <p class="text-lg text-gray-700">
                            {{ service.description }}
                        </p>
                        <ul class="list-disc list-inside text-lg text-gray-700">
                            <li v-for="(item, idx) in service.list" :key="idx">
                                {{ item }}
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>

    </div>
</template>