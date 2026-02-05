<template>
    <div class="relative py-24 overflow-hidden bg-linear-to-r from-blue-900/50 to-cyan-900/50" id="services">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16" data-aos="fade-up">
                <h2 class="text-4xl font-bold text-white mb-6 tracking-tight">
                    <span class="text-transparent bg-clip-text bg-linear-to-r from-blue-500 to-cyan-500">My Services</span>
                </h2>
                <p class="mt-4 text-blue-300 max-w-3xl mx-auto text-lg leading-relaxed">
                    I offer a range of web development services to help you build and enhance your online presence with modern, responsive solutions.
                </p>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8" data-aos="fade-up" data-aos-delay="200">
                <div v-for="(service, index) in services" :key="service.id" :data-aos="'fade-up'" :data-aos-delay="index * 100">
                    <div class="group relative bg-gray-800 rounded-2xl border border-blue-500/20 shadow-lg hover:shadow-2xl transition-all duration-500 hover:-translate-y-2">
                        <div class="absolute inset-0 bg-linear-to-r from-blue-500/10 to-cyan-500/10 rounded-2xl opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                        <div class="relative p-8">
                            <div class="flex items-center justify-center w-16 h-16 mb-6 group-hover:bg-blue-500 group-hover:text-white transition-all duration-300 rounded-full shadow-lg bg-gray-800/50">
                                <component :is="service.icon" class="w-8 h-8 text-blue-400 group-hover:text-cyan-300 transition-colors duration-300"></component>
                            </div>
                            <h3 class="text-xl font-bold text-white mb-4 group-hover:text-cyan-300 transition-colors duration-300">{{ service.name }}</h3>
                            <p class="text-blue-300 leading-relaxed">{{ service.description }}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import { ref } from 'vue';
import {
    CodeBracketIcon,
    ComputerDesktopIcon, DocumentTextIcon, EnvelopeIcon
} from '@heroicons/vue/16/solid';

export default {
    setup() {
        const services = ref([
            {
                id: 1,
                icon: CodeBracketIcon,
                name: 'Web Development',
                description: 'Building responsive and dynamic websites using modern technologies like Vue.js, React, and Node.js.'
            },
            {
                id: 2,
                icon: ComputerDesktopIcon,
                name: 'UI/UX Design',
                description: 'Designing user-friendly interfaces and experiences that engage and delight users.'
            },
            {
                id: 3,
                icon: DocumentTextIcon,
                name: 'Consultation',
                description: 'Providing expert advice on web development best practices, performance optimization, and technology selection.'
            },
            {
                id: 4,
                icon: EnvelopeIcon,
                name: 'SEO Optimization',
                description: 'Improving website visibility and search engine rankings through effective SEO strategies.'
            }
        ]);

        return { services };
    }
}
</script>
