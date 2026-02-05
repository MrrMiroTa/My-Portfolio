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
                            <a href="{{ project.link }}" 
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
        description: 'A full-stack e-commerce platform built with Vue.js, Laravel, and MySQL, featuring user authentication, payment processing, and real-time inventory management.',
        link: '#project1'
    },
    {
        id: 2,
        title: 'Task Management App',
        description: 'A collaborative task management application with real-time updates, drag-and-drop functionality, and team collaboration features built with Vue.js and Firebase.',
        link: '#project2'
    },
    {
        id: 3,
        title: 'Portfolio Website',
        description: 'A modern, responsive portfolio website showcasing web development projects with smooth animations and interactive elements using Vue.js and Tailwind CSS.',
        link: '#project3'
    },
    {
        id: 4,
        title: 'Weather Dashboard',
        description: 'A weather dashboard application with real-time weather data, interactive maps, and location-based forecasts using Vue.js and OpenWeather API.',
        link: '#project4'
    },
    {
        id: 5,
        title: 'Blog Platform',
        description: 'A content management system for blogging with user authentication, rich text editing, and social sharing features built with Vue.js and Strapi.',
        link: '#project5'
    },
    {
        id: 6,
        title: 'Chat Application',
        description: 'A real-time chat application with private messaging, group chats, and file sharing capabilities using Vue.js, Socket.io, and Node.js.',
        link: '#project6'
    }
]);
</script>
