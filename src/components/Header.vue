<script setup>
import { Menu, X } from 'lucide-vue-next';
import { ref } from 'vue';

    const isMenuOpen = ref(false)

    const menuItems = [
        {name: 'Education', href: '#education'},
        {name: 'Certificates', href: '#certificate'},
        {name: 'About', href: '#about'},
        {name: 'Skills', href: '#skill'},
        {name: 'Projects', href: '#project'}
    ]

    const scrollToSection = (href) => {
        isMenuOpen.value = false

        const element = document.querySelector(href)

        if(element){
            element.scrollIntoView({behavior: 'smooth'})
        }
    }
</script>

<template>
    <header class="relative z-50 px-6 py-7">
        <div class="max-w-7xl flex justify-between items-center">
            <!-- Logo -->
             <div class='text-white text-3xl font-black cursor-pointer'>
                Portfolio<span class="text-primary">.</span>
             </div>

             <nav class="hidden md:flex items-center gap-10">
                <ul class="flex gap-8">
                    <li v-for="menu in menuItems" :key="menu.name"><button @click="scrollToSection(menu.href)" class="text-gray-300 hover:text-white">{{ menu.name }}</button></li>
                </ul>

                <button class="text-white text-nowrap bg-primary p-2 rounded-lg" @click="scrollToSection('#contact')">Contact Me</button>
             </nav>

             <!-- menu button  -->
              <button class="md:hidden text-white" @click="isMenuOpen = !isMenuOpen">
                <Menu v-if="!isMenuOpen" :size="32" />
                <X v-else :size="32" />
              </button>
        </div>

        <div v-if="isMenuOpen" class="fixed inset-0 bg-black/60 backdrop-blur-sm md:hidden" @click="isMenuOpen = false">
            <div class="fixed top-0 right-0 h-full w-80 bg-[#111827] z-50 transform transition-transform duration-300 md:hidden p-4" @click="isMenuOpen ? 'translate-x-0' : 'translate-x-full'">
                <button class="self-end text-white mb-10" @click="isMenuOpen = false"><X :size="32" /></button>

                <ul class="flex flex-col gap-6">
                    <li v-for="menu in menuItems" :key="menu.name">
                        <button @click="scrollToSection(menu.href)" class="text-white">{{ menu.name }}</button>
                    </li>

                    <li>
                        <button class="text-white bg-primary rounded-lg p-2 w-full" @click="scrollToSection('#contact')">Contact Me</button>
                    </li>
                </ul>
            </div>
        </div>
    </header>
</template>