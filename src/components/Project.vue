<script setup>
    import proj1 from '../assets/proj1.png'
    import proj2 from '../assets/proj2.png'
    import proj3 from '../assets/proj3.png'
    import proj4 from '../assets/proj4.png'

    const projects = [
        {
            id: 1,
            image: proj1,
            title: "CyberCove",
            desc: "CyberCove is a discussion forum and educational platform focused on Cyber Security, designed as part of the Web Design Competition at ITCC 2025, organized by Udayana University in Bali.",
            tech: ['HTML', 'CSS', 'JS']
        },
        {
            id: 2,
            image: proj2,
            title: "SRINFO",
            desc: "SRINFO SSRI Information is a website I created to display information about my school.",
            tech: ['HTML', 'CSS', 'JS', 'Laravel']
        },
        {
            id: 3,
            image: proj3,
            title: "Englify",
            desc: "ENGLIFY is an educational application about English",
            tech: ['Dart', 'Flutter']
        },
        {
            id: 4,
            image: proj4,
            title: "PresentApp",
            desc: "A modern Classroom Attendance Application built with Flutter, Drift Database, and Gemini AI to help manage student attendance in a fast, lightweight, and efficient way.",
            tech: ['Dart', 'Flutter', 'Drift Database', 'Gemini API']
        }
    ]
</script>

<template>
    <section class="pb-25 pt-25 relative w-full" id="project">
        <div class="flex flex-col gap-10">
            <div class="flex flex-col gap-4 items-center justify-center">
                <h1 class="text-5xl font-black text-white text-center">Projects.</h1>
                <div class="h-1 m-auto w-24 rounded-full bg-primary"></div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 p-6">
                <div v-for="project in projects" :key="project.id" class="rounded-xl items-stretch bg-[#242426] overflow-hidden min-h-40">
                    <img :src="project.image" alt="" class="w-full h-50 object-cover opacity-80">

                    <div class="flex flex-col gap-4 p-4 justify-between min-h-40">
                        <h1 class="text-white font-black text-2xl">{{ project.title }}</h1>
                        <p class="text-gray-400 font-bold text-[0.7rem]">{{ project.desc }}</p>
                        <div class="flex flex-row gap-2 items-center">
                            <div v-for="tech in project.tech" class="p-2 rounded-md bg-primary">
                                <p class="text-white font-black text-[0.5rem]">{{ tech }}</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>