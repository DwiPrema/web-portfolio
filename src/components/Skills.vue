<script setup>
import { BriefcaseBusiness, Building2, Info } from '@lucide/vue';

    const skills = [
        {
            id: 1,
            name: "Dart & Flutter",
            width: "95%",
        },
        {
            id: 2,
            name: "Firebase",
            width: "85%",
        },
        {
            id: 3,
            name: "Supabase",
            width: "70%",
        },
        {
            id: 4,
            name: "Javascript",
            width: "80%",
        },
        {
            id: 5,
            name: "Vue Js",
            width: "80%",
        },
        {
            id: 6,
            name: "Laravel",
            width: "65%",
        },
    ]

    const workExperiences = [
        {
            id: 1,
            role: "Mobile & Web Dev",
            status: "Internship",
            company: "Diskominfos Kota Denpasar",
            date: "June - December"
        }
    ]
</script>


<template>
    <section class="pb-25 pt-25 relative w-full" id="skill">
        <div class="w-full relative px-5 sm:px-8 md:px-12 lg:px-8 max-w-5xl lg:max-w-7xl mx-auto">
            <div class="grid lg:grid-cols-2 gap-20 xl:gap-14 relative lg:max-w-none max-w-2xl md:max-w-3xl mx-auto items-start">
                <div class="lg:py-6 flex flex-col gap-4">
                    <h1 class="font-black text-5xl text-white mb-10 text-center lg:text-left">Technical <span class="text-primary">Skills</span></h1>
 data-aos="fade-up-right"
                    <div v-for="skill in skills" :key="skill.id" class="p-2 flex flex-col gap-2" data-aos="fade-up-right">
                        <div class="flex flex-row items-center justify-between">
                            <p class="text-white font-bold">{{ skill.id }}. {{ skill.name }}</p>
                            <p class="text-primary">{{ skill.width }}</p>
                        </div>

                        <div class="w-full bg-[#111a3e] h-1.5 rounded-full">
                            <div class="bg-linear-to-r from-primary to-white shadow-[0_0_10px_#06a2c2] h-full rounded-full" :style="{width: skill.width}"></div>
                        </div>
                    </div>
                </div>

                <div class="lg:py-6 flex flex-col gap-4">
                    <h1 class="font-black text-5xl text-white mb-10 text-center lg:text-left">Work <span class="text-primary">Experience</span></h1>

                    <div v-for="work in workExperiences" :key="work.id" class="p-4 gap-2 bg-[#111a3e] rounded-xl" data-aos="fade-up-left">
                        <div class="flex flex-row items-center gap-4">
                            <div class="bg-black rounded-md p-4">
                                <BriefcaseBusiness class="text-primary" :size="16"/>
                            </div>

                            <div class="flex flex-col gap-3 w-full">
                                <div class="flex sm:flex-row flex-col items-start justify-between ">
                                    <h1 class="text-white font-black text-[1rem]">{{ work.role }}</h1>
                                    <p class="text-gray-400 text-[0.7rem] font-bold">{{ work.date }}</p>
                                </div>
                                <div class="flex sm:flex-row flex-col sm:items-center items-start sm:gap-4 gap-1">
                                    <div class="flex flex-row items-center gap-2">
                                        <Building2 class="text-primary" :size="16"/>
                                        <p class="text-gray-400 text-[0.7rem] font-bold">{{ work.company }}</p>
                                    </div>

                                    <div class="flex flex-row items-center gap-2">
                                        <Info class="text-primary" :size="16"/>
                                        <p class="text-gray-400 text-[0.7rem] font-bold">{{ work.status }}</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>