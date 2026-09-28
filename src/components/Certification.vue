<script setup>
import { Award, ExternalLink, ShieldCheck } from '@lucide/vue';

    const certifications = [
        {
            id: 1,
            institusion: "ITCC 2025",
            title: "Finalis Web Design Competition ITCC 2025",
            description: "Selected as a finalist in the High School/Vocational School Web Design Competition at ITCC 2025, organized by Udayana University.",
            link: "https://drive.google.com/file/d/12y0jdL3AQVXuo2ej77ZYH5CbsH5U5hVy/view?usp=drive_link"
        },
        {
            id: 2,
            institusion: "ITCC 2025",
            title: "Participant of Web Design Competition ITCC 2025",
            description: "Be a participant web design competition that organized by Udayana University",
            link: "https://drive.google.com/file/d/1EWCsiiOUvY5t0aJr5IIiOPseDOr9KJp3/view?usp=drive_link",
        },
        {
            id: 3,
            institusion: "Sitefest 2025",
            title: "Web Design Competition Sitefest 2025",
            description: "Be a participant web design competition that organized by Primakara University",
            link: "https://drive.google.com/file/d/132A3QSzoGsElFaHsXuA3GdhUjm-ho-w2/view?usp=drive_link",
        }
    ]

    const openExternalUrl = (link) => {
        window.open(link, '_blank', 'noopener, noreferrer')
    }
</script>

<template>
    <section class="pb-25 pt-25 relative w-full" id="certificate">
        <div class="w-full relative px-5 sm:px-8 md:px-12 lg:px-8 max-w-5xl lg:max-w-7xl mx-auto flex flex-col gap-20">
            <div>
                <p class="text-primary font-medium text-center lg:text-left">Achievements</p>
                <h1 class="text-white font-black text-5xl text-center lg:text-left">Certifications.</h1>
            </div>

            <div class="grid md:grid-cols-3 gap-8 items-stretch">
                <div v-for="certification in certifications" :key="certification.id" class="flex md:h-full h-min">
                    <div class="relative bg-[#111a3e] p-6 rounded-xl md:min-h-65 w-full group hover:scale-103 duration-300 transition-all ease-in-out">
                        <div class="p-3 rounded-md bg-primary w-min absolute -top-3 -right-3 group-hover:rotate-15 transition-all ease-in-out duration-300">
                            <Award class="text-white" :size="18"/>
                        </div>

                        <div class="flex flex-col gap-4 justify-between md:min-h-65 h-full">
                            <div class="flex flex-row gap-2 items-center">
                                <ShieldCheck class="text-primary" :size="16"/>
                                <p class="text-gray-400 text-[0.8rem] font-black">{{ certification.institusion }}</p>
                            </div>
                            
                            <h1 class="text-white font-black text-xl">{{ certification.title }}</h1>

                            <p class="text-gray-400 text-[0.8rem]">{{ certification.description }}</p>

                            <a @click="openExternalUrl(certification.link)" class="text-primary flex flex-row gap-2 items-center text-[0.8rem] cursor-pointer hover:underline hover:text-[#0b9a17] transition-all ease-in-out duration-300">
                                <p>View Certificate</p>
                                <ExternalLink :size="16"/>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>