<template lang="html">
    <div class="relative py-24 overflow-hidden bg-linear-to-r from-blue-900/50 to-cyan-900/50"  id="projects">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16" data-aos="fade-up">
                <h2 class="text-4xl font-bold text-white mb-6 tracking-tight">
                    <span class="text-transparent bg-clip-text bg-linear-to-r from-blue-500 to-cyan-500">My Projects</span>
                </h2>
                <p class="mt-4 text-blue-300 max-w-3xl mx-auto text-lg leading-relaxed">
                    Here are some of the projects I've worked on, showcasing my skills and experience in web development.
                </p>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8" data-aos="fade-up" data-aos-delay="200">
                <div v-for="(project, index) in projects" :key="project.id" :data-aos="'fade-up'" :data-aos-delay="index * 100">
                    <div class="group relative bg-gray-800 rounded-2xl border border-blue-500/20 shadow-lg hover:shadow-2xl transition-all duration-500 hover:-translate-y-2">
                        <div class="absolute inset-0 bg-linear-to-br from-blue-500/10 to-cyan-500/10 rounded-2xl opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                        <div class="relative p-8">
                            <h3 class="text-xl font-bold text-white mb-4 group-hover:text-cyan-300 transition-colors duration-300">{{ project.title }}</h3>
                            <p class="text-blue-300 leading-relaxed mb-6">{{ project.description }}</p>
                            <a :href="project.link" target="_blank" 
                                class="inline-block border-2 border-blue-400 bg-blue-500 px-6 py-3 rounded-xl text-white font-medium hover:bg-blue-400 transition-all duration-300">
                                View Project
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script setup>
import { ref } from 'vue';

const projects = ref([
    {
        id: 1,
        title: 'E-Commerce Platform',
        description: 'A full-stack e-commerce platform built with React.js, Laravel, and MySQL, featuring user authentication, payment processing, and real-time inventory management.',
        link: 'https://e-commerceshop-three.vercel.app/'
    },
    {
        id: 2,
        title: 'Calculator App',
        description: 'A simple yet elegant calculator application built with Vue.js and Tailwind CSS, featuring a clean UI and responsive design.',
        link: 'https://calculator-app-uzita.vercel.app/'
    },
    {
        id: 3,
        title: 'Portfolio Website',
        description: 'A modern, responsive portfolio website showcasing web development projects with smooth animations and interactive elements using Vue.js and Tailwind CSS.',
        link: 'https://portfolio-sophors.vercel.app/'
    },
    {
        id: 4,
        title: 'News Website',
        description: 'A news website with real-time updates, categorized articles, and a responsive design using Vue.js and Tailwind CSS.',
        link: 'https://news-by-uzita.vercel.app/'
    },
    {
        id: 5,
        title: 'To Do List App',
        description: 'A simple yet elegant to-do list application built with Vue.js and Tailwind CSS, featuring task management and a clean UI.',
        link: 'https://mrrmirota.github.io/To-Do-List/'
    },
    
]);
</script>
