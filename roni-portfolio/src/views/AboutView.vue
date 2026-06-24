<script setup>
import backgroundImage from '@/assets/camp.jpg'
</script>

<template>
    <div class="relative bg-cover bg-center bg-no-repeat" :style="{ backgroundImage: `url(${backgroundImage})` }">
        <div class="absolute inset-0 bg-black/50 backdrop-blur-sm"></div>
        <div class="relative z-10 flex flex-col items-center justify-center gap-8 font-montserrat pt-16 bg-[rgb(220,220,230,0.6)]">
            <div class="w-full flex flex-row pt-32 px-12 justify-between items-center gap-8">
                <div class="w-3/4 flex flex-col gap-4 justify-center">
                    <h1 class="font-montserrat text-4xl text-left text-black">
                        I spent over a decade implementing Equity & Inclusion systems and trainings at independent schools, and here’s what I realized:
                    </h1>
                    <h1 class="font-montserrat text-4xl text-left text-black italic font-semibold">
                        The real culture shift happens one teacher at a time.
                    </h1>
                </div>
                <div class="w-1/4 justify-center">
                    <img src="@/assets/crop-photo.jpg" alt="Cover Photo" class="aspect-square object-cover rounded-full object-cover shadow-lg border-gray-2">
                </div>
            </div>
            <div class="h-12"></div>
            <div class="bg-[rgb(250,250,250,0.3)] px-12 py-8 h-full">
                <p class="font-montserrat text-lg">
                    In order to create learning environments where young people feel a deep sense of belonging, we need to properly resource our teachers. I offer a framework that involves observing oneself (with gentleness!) and disrupting old patterns of thinking, responding and communicating; as well as incorporating tools that will increase student’s motivation, accountability, and potential for growth. 
                </p>
                <p class="font-montserrat text-lg pt-12">
                    Since 2006, I have worked in Bay Area private schools as Director of Social Justice & Inclusion, Dean of Student Life, Service Learning Coordinator, and DEIB Consultant. I established a schoolwide Restorative Justice program, and practiced as a credentialed Restorative Justice Practitioner. Since 2024, I have facilitated year-long Restorative Teaching Cohorts for faculty. I believe the experience of teaching can be a profound catalyst for personal discovery and relational evolution – and I am passionate about supporting other educators on this journey!
                </p>
                <v-btn variant="outlined" rounded="xl" size="large" append-icon="mdi-email-arrow-right-outline" :href="googleFormLink" target="_blank" color="#006622" class="!bg-[rgba(0,102,34,0.1)] mt-12">
                    Email Me
                </v-btn>
            </div>
        </div>
    </div>
</template>