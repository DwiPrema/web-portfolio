<script setup>

</script>

<template>
    <section class="relative w-full pt-25 pb-25" id="about">
        <div class="absolute h-64 top-0 inset-x-0 flex items-start">
            <div class="w-2/3 h-24 bg-linear-to-br from-[#0cac19] blur-2xl opacity-40">

            </div>

            <div class="h-20 w-3/4 bg-linear-to-r from-[#4fff28] opacity-40 invisible blur-2xl"></div>
        </div>

        <div class="w-full relative px-5 sm:px-8 md:px-12 lg:px-8 max-w-5xl lg:max-w-7xl mx-auto">
            <div class="grid lg:grid-cols-2 gap-20 xl:gap-14 relative lg:max-w-none max-w-2xl md:max-w-3xl mx-auto items-center">
                <div class="lg:py-6">
                    <div class="text-center lg:text-left">
                        <h1 class="text-white font-black text-5xl">More <span class="text-primary font-black text-5xl">About </span>Me</h1>
                    </div>
                    <p class="text-gray-300 pt-8 text-center lg:text-left m-auto lg:m-0 max-w-xl">When I’m not coding or debugging Flutter apps, I like to keep my momentum going by learning new tools and concepts. Right now, my focus is on mastering Supabase & PostgreSQL to build more dynamic and scalable backends. I treat every project as an opportunity to grow, trusting that a patient and wholehearted process always leads to the best results.</p>
                    <div class="flex pt-8 gap-3 flex-row items-stretch justify-center lg:justify-start">
                        <div class="relative bg-[#111a3e] p-6 rounded-xl md:min-h-20 w-min hover:scale-103 duration-300 transition-all ease-in-out justify-center items-center">
                            <h1 class="text-2xl font-black text-primary">+2</h1>
                            <span class="text-gray-400 font-black text-[0.6rem]">YEARS</span>
                        </div>
                        <div class="relative bg-[#111a3e] p-6 rounded-xl md:min-h-20 w-min hover:scale-103 duration-300 transition-all ease-in-out justify-center items-center">
                            <h1 class="text-2xl font-black text-primary">+5</h1>
                            <span class="text-gray-400 font-black text-[0.6rem]">PROJECTS</span>
                        </div>
                    </div>
                </div>

                <!-- IMAGE -->
                <div class="lg:h-full md:flex">
                        <div
                            class="flex w-full h-110 min-h-110 lg:w-full lg:h-full items-center relative justify-center">
                            <div class="absolute h-full z-10 rounded-full border border-primary">
                                <div class="-translate-x-3 -translate-y-3 w-full h-full rounded-full overflow-hidden">
                                    <img src="../assets/about.jpeg" alt=""
                                    class="w-full h-full object-cover bg-center transition-all duration-500 ease-in-out hover:scale-110"></div>
                            </div>
                        </div>
                    </div>
            </div>
        </div>
    </section>
</template>