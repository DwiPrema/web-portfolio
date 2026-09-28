<script setup>
import { Calendars, CircleCheck, GraduationCap } from '@lucide/vue';

const educationData = [
    {
        title: "SMKN 1 SUKAWATI",
        description: "Majoring in Software Engineering (RPL). Actively expanding my technical expertise while enthusiastically participating in various coding and technology competitions.",
        time: "2024-present"
    },
    {
        title: "SMPN 3 SUKAWATI",
        description: "Completed junior high school education, building a strong academic foundation and developing an early interest in technology and problem-solving.",
        time: "2021-2024"
    }
]
</script>

<template>
    <section class="pb-25 pt-25 relative w-full" id="education">
        <div class="w-full relative px-5 sm:px-8 md:px-12 lg:px-8 max-w-5xl lg:max-w-7xl mx-auto flex flex-col gap-20">
            <div>
                <p class="text-primary font-medium text-center lg:text-left">Learning path</p>
                <h1 class="text-white font-black text-5xl text-center lg:text-left">Education.</h1>
            </div>

            <div class="w-full relative px-5 max-w-5xl lg:max-w-7xl mx-auto">
                <div
                    class="grid lg:grid-cols-3 gap-32 relative lg:max-w-none max-w-2xl md:max-w-3xl mx-auto items-center">
                    <div class="lg:h-full md:flex lg:col-span-1" data-aos="zoom-in">
                        <div
                            class="flex w-full h-96 min-h-96 lg:w-full lg:h-full items-center relative justify-center">
                            <div class="absolute h-full lg:w-full z-10 rounded-3xl border border-primary">
                                <div class="-translate-x-3 -translate-y-3 w-full h-full rounded-3xl overflow-hidden">
                                    <img src="../assets/educ.jpg" alt=""
                                    class="w-full h-full object-cover bg-center transition-all duration-500 ease-in-out hover:scale-110"></div>
                            </div>
                        </div>
                    </div>

                    <div class="flex flex-col gap-4 lg:col-span-2">
                        <div v-for="data in educationData" :key="data.title" data-aos="fade-up">
                            <div class="bg-[#1f1641] rounded-xl p-6 flex flex-col gap-6">
                                <div class="flex sm:flex-row justify-between items-start flex-col gap-4">
                                    <div class="flex flex-row gap-4 items-start">
                                        <div class="p-2 rounded-xl border border-white w-min bg-black">
                                            <GraduationCap class="text-primary"/>
                                        </div>

                                        <h1 class="font-bold text-white">{{ data.title }}</h1>
                                    </div>

                                    <div class="bg-black border-[0.2px] border-gray-300 rounded-full flex flex-row gap-2 items-center pr-2 pl-2 pt-1 pb-1">
                                        <Calendars class="text-primary" :size="16"/>
                                        <p class="text-white font-bold text-[0.6rem]">{{ data.time }}</p>
                                    </div>
                                </div>

                                <div>
                                    <p class="text-gray-300 font-[0.5rem]">{{ data.description }}</p>
                                </div>
                                
                                <div class="flex flex-row items-center gap-1">
                                    <CircleCheck class="text-primary" :size="16"/>
                                    <p class="text-primary text-[0.8rem] font-bold">Academic Excellence</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>