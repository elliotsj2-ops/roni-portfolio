<script setup lang="ts">
import backgroundImage from '@/assets/camp.jpg'
import { ref } from 'vue'

const testimonials = ref([
    {
        author: "Lauren Cook, College Counselor",
        content: "Over the past decade I've had the privilege of working alongside Roni in social justice and anti-bias education, and I consistently come away impressed by her thoughtfulness, warmth, and commitment to growth. She has the remarkable ability to create spaces where people feel invited into meaningful change while staying grounded in the latest practices. Her ability to call people in - with both honesty and care - is one of her greatest strengths."
    },
    {
        author: "Josh Buchin, Dean of Students & Jewish Studies Teacher",
        content: "It was great to have space to process teaching with other colleagues and to be prompted to reflect on my process as a teacher. And I loved learning practical skills that I could use to improve my teaching."
    },
    {
        author: "Amy Dean, Chair of Math & Science Department",
        content: "Roni’s guidance and resources were both amazing and action-oriented."
    },
    {
        author: "Adi Alouf, Director of Jewish & Student Life, Jewish Studies Teacher",
        content: "Roni, with her deep wisdom and warmth, leads and models restorative approaches to teaching, learning, and community that are nothing short of transformational. Through faculty workshops and ongoing learning cohorts, she helped educators at JCHS develop practical tools for cultivating classrooms and a school culture rooted in humanity, student empowerment, and belonging. Roni guides communities and institutions in thinking and developing the skills for what deep learning truly requires – not only rigorous instruction, but relationships that enable every student and educator to flourish. Her work has fundamentally shaped the culture of our school."
    }
]);
</script>

<template>
    <div class="relative bg-cover bg-center bg-no-repeat" :style="{ backgroundImage: `url(${backgroundImage})` }">
        <div class="absolute inset-0 bg-black/50 backdrop-blur-sm"></div>
        <div class="relative z-10 flex flex-col items-center justify-center gap-8 font-montserrat pt-16 bg-[rgb(220,220,230,0.6)]">
            <div class="w-full flex flex-row pt-32 px-12 justify-between items-center gap-8">
                <div class="w-1/2 md:w-3/4 flex flex-col gap-4 justify-center">
                    <h1 class="font-montserrat text-4xl text-left text-black">
                        I spent over a decade implementing Equity & Inclusion systems and trainings at independent schools, and here’s what I realized:
                    </h1>
                    <h1 class="font-montserrat text-4xl text-left text-black italic font-semibold">
                        The real culture shift happens one teacher at a time.
                    </h1>
                </div>
                <div class="w-1/2 md:w-1/4 justify-center">
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
                <v-btn variant="outlined" rounded="xl" size="large" append-icon="mdi-email-arrow-right-outline" href="mailto:ronibendavid@gmail.com" target="_blank" color="#006622" class="!bg-[rgba(0,102,34,0.1)] mt-12">
                    Email Me
                </v-btn>

                <div>
                    <div class="flex flex-row items-center justify-center w-full">
                        <div class="flex-grow border-t border-black"></div>
                        <span class="text-4xl font-semibold text-black py-8 px-12">
                            Testimonials
                        </span>
                        <div class="flex-grow border-t border-black"></div>
                    </div>

                    <div class="flex flex-col md:flex-row gap-8 py-8">
                        <div v-for="(testimonial, index) in testimonials" :key="index" class="flex flex-col gap-4 md:w-full p-8 bg-[rgb(220,220,230,0.6)] rounded-lg shadow-md">
                            <p class="text-xl text-gray-700 font-playfair">
                                "{{ testimonial.content }}"
                            </p>
                            <h2 class="font-italic text-xl font-bold text-gray-800">
                                —&nbsp;&nbsp;{{ testimonial.author }}
                            </h2>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>