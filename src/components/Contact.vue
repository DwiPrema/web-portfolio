<script setup>
import { Mail, MapPin, Phone } from '@lucide/vue';
import { Linkedin } from 'lucide-vue-next';
import { reactive, ref } from 'vue';

const contacts = [
    {
        id: 1,
        name: "Email",
        value: "madedwiprema08@gmail.com",
        icon: Mail,
        link: "https://mail.google.com/mail/?view=cm&fs=1&to=madedwiprema08@gmail.com"
    },
    {
        id: 2,
        name: "Phone",
        value: "+62-8787-3974-618",
        icon: Phone,
        link: "tel: +6287873974618"
    },
    {
        id: 3,
        name: "LinkedIn",
        value: "linkedin.com/in/dwi-premayasa-60646738a/",
        icon: Linkedin,
        link: "https://www.linkedin.com/in/dwi-premayasa-60646738a/"
    },
    {
        id: 4,
        name: "Location",
        value: "Bali, Indonesia",
        icon: MapPin,
        link: null,
    },
]

const formData = reactive({
    email: '',
    subject: '',
    message: '',
})

const isSubmitting = ref(false)

const handleSubmit = async () => {
    isSubmitting.value = true

    try {
        formData.email = '',
        formData.subject = '',
        formData.message = ''
    } catch (e) {
        alert('Failed to send message. Please try again later!')
    } finally {
        isSubmitting.value = false
    }
}
</script>


<template>
    <section class="pb-25 pt-25 relative w-full flex flex-col gap-20" id="contact">
        <div class="flex flex-col gap-4 items-center justify-center">
            <h1 class="text-5xl font-black text-white text-center">Let's Connect.</h1>
            <div class="h-1 m-auto w-24 rounded-full bg-primary"></div>
        </div>

        <div class="w-full relative px-5 sm:px-8 md:px-12 lg:px-8 max-w-5xl lg:max-w-7xl mx-auto">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-24">
                <div class="flex flex-col">
                    <p class="text-gray-400 text-[1rem] font-bold mb-12">Feel free to reach out if you want to collaborate, have a question, or just want to connect. I’m always open to discussing new projects and tech!</p>

                    <div class="lg:px-12 flex flex-col gap-6">
                        <div v-for="contact in contacts" :key="contact.id"
                            class="flex flex-row items-center gap-4 group">
                            <component :is="contact.icon"
                                class="text-primary group-hover:scale-105 duration-300 transition-all ease-in-out"
                                :size="16"></component>

                            <div class="flex flex-col items-start">
                                <h1 class="text-white text-sm font-black">{{ contact.name }}</h1>
                                <a :href="contact.link" target="_blank" rel="noopener noreferrer" class="text-gray-400 text-[0.7rem]">{{
                                    contact.value }}</a>
                            </div>
                        </div>
                    </div>

                </div>

                <div class="p-8 rounded-2xl bg-[#111a3e]">
                    <form @submit.prevent="handleSubmit">
                        <!-- Email -->
                        <div class="flex flex-col gap-2 items-start mb-5">
                            <label for="email" class="text-white text-sm font-black">Email</label>
                            <input type="email" id="email" v-model="formData.email" placeholder="your@gmail.com" class="bg-gray-700 p-2 w-full border border-gray-600 focus:outline-none focus:border-primary rounded-sm transition-colors placeholder:text-gray-400 text-[0.7rem] text-white">
                        </div>

                        <!-- Message  -->
                         <div class="flex flex-col gap-2 items-start mb-5">
                            <label for="message" class="text-white text-sm font-black">Message</label>
                            <textarea id="message" v-model="formData.message" rows="4" placeholder="Enter your message here!" class="bg-gray-700 p-2 w-full border border-gray-600 focus:outline-none focus:border-primary rounded-sm transition-colors placeholder:text-gray-400 text-[0.7rem] text-white"></textarea>
                        </div>

                        <!-- Button  -->

                        <button type="submit" :disabled="isSubmitting" class="bg-primary rounded-md text-white text-sm w-full text-center font-black p-2 cursor-pointer hover:bg-[#129e1d] transition-all ease-in-out duration-300 disabled:opacity-50 disabled:cursor-not-allowed">{{ isSubmitting ? "Sending..." : "Send Message" }}</button>
                    </form>
                </div>
            </div>
        </div>
    </section>
</template>