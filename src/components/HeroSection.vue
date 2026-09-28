<script setup>
import { Download } from 'lucide-vue-next';
</script>

<template>
    <section class="relative w-full pt-10 pb-25">
        <div class="absolute h-64 top-0 inset-x-0 flex items-start">
            <div class="w-2/3 h-24 bg-linear-to-br from-[#0cac19] blur-2xl invisible opacity-40">

            </div>

            <div class="h-20 w-3/4 bg-linear-to-r from-[#4fff28] opacity-40 blur-2xl"></div>
        </div>

        <div class="w-full relative px-5 sm:px-8 md:px-12 lg:px-8 max-w-5xl lg:max-w-7xl mx-auto">
            <div class="grid lg:grid-cols-2 gap-20 xl:gap-14 relative pt-24 lg:max-w-none max-w-2xl md:max-w-3xl mx-auto">
                <div class="lg:py-6">
                    <div class="text-center lg:text-left">
                        <h1 class="text-white font-black text-5xl">Hello, I am <span class="bg-linear-to-r from-primary to-white font-black bg-clip-text text-transparent text-5xl">Dwi </span>👋</h1>
                    </div>
                    <p class="text-gray-300 pt-8 text-center lg:text-left m-auto lg:m-0 max-w-xl">I am a passionate Software Engineering student from Indonesia specializing in Dart and Flutter mobile development as well as web technologies like Laravel and MySQL. I am currently expanding my skill set into Supabase and PostgreSQL, driven by patience and hard work to build a career as a versatile Mobile and Web Developer.</p>
                    <div class="flex pt-8 gap-3 flex-col sm:flex-row">
                        <button class="bg-primary rounded-full sm:w-max m-auto lg:m-0 relative w-full sm:min-w-50 p-4 hover:bg-[#129e1d] hover:scale-103 transition-all ease-in-out duration-300">
                            <div class="flex flex-row gap-4 justify-center items-center relative">
                                <p class="text-white">Hire Me</p>
                            </div>
                        </button>
                        <button class="border border-primary rounded-full sm:w-max m-auto lg:m-0 relative w-full sm:min-w-50 p-4 hover:scale-103 transition-all ease-in-out duration-300">
                            <div class="flex flex-row gap-4 justify-center items-center relative">
                                <Download class="text-primary" :size="16"/>
                                 <a href="../assets/CV I Made Dwi Premayasa (Flutter Intern).pdf" download="../assets/CV I Made Dwi Premayasa (Flutter Intern).pdf" class="text-primary">Download Resume</a>
                            </div>
                        </button>
                    </div>
                </div>

                <!-- IMAGE -->
                <div class="lg:h-full md:flex">
                    <div class="flex w-full h-96 min-h-96 lg:min-h-[none] lg:w-full lg:h-full items-center relative justify-end">
                            <div class="absolute h-full z-10 rounded-[30%_70%_70%_30%/30%_30%_70%_70%] border p-2 border-primary">
                                <img src="../assets/hero.jpg" alt="" class="w-full h-full rounded-[30%_70%_70%_30%/30%_30%_70%_70%] object-cover bg-center" width="500" height="auto">
                            </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>