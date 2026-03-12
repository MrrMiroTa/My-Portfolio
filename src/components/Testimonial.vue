<template>
    <div class="relative py-24 overflow-hidden bg-gradient-to-r from-blue-900/50 to-cyan-900/50" id="testimonials">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16" data-aos="fade-up">
                <h2 class="text-4xl font-bold text-white mb-6 tracking-tight">
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-500 to-cyan-500">Testimonials</span>
                </h2>
                <p class="mt-4 text-blue-300 max-w-3xl mx-auto text-lg leading-relaxed">
                    What clients and colleagues say about working with me.
                </p>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8" data-aos="fade-up" data-aos-delay="200">
                <div v-for="(testimonial, index) in testimonials" :key="testimonial.id" 
                     :data-aos="'fade-up'" 
                     :data-aos-delay="index * 100"
                     class="group">
                    <div class="relative bg-gray-800/80 backdrop-blur-sm rounded-2xl p-8 border border-blue-500/20 shadow-lg hover:shadow-2xl transition-all duration-500 hover:-translate-y-2 h-full">
                        <div class="absolute inset-0 bg-gradient-to-br from-blue-500/5 to-cyan-500/5 rounded-2xl opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                        <div class="relative">
                            <div class="flex items-center gap-1 mb-4">
                                <svg v-for="i in 5" :key="i" class="w-5 h-5 text-yellow-400" fill="currentColor" viewBox="0 0 20 20">
                                    <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                                </svg>
                            </div>
                            <p class="text-blue-200 leading-relaxed mb-6 italic">"{{ testimonial.message }}"</p>
                            <div class="flex items-center gap-4">
                                <div class="w-12 h-12 rounded-full bg-gradient-to-r from-blue-500 to-cyan-500 flex items-center justify-center text-white font-bold text-lg">
                                    {{ testimonial.name.charAt(0) }}
                                </div>
                                <div>
                                    <h4 class="text-white font-semibold">{{ testimonial.name }}</h4>
                                    <p class="text-blue-400 text-sm">{{ testimonial.position }}</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const testimonials = ref([
    {
        id: 1,
        name: 'John Smith',
        position: 'CEO, Tech Solutions',
        message: 'Sophors delivered an outstanding e-commerce platform that exceeded our expectations. His attention to detail and ability to meet deadlines is impressive.'
    },
    {
        id: 2,
        name: 'Sarah Johnson',
        position: 'Product Manager',
        message: 'Working with Sophors was a great experience. He understood our requirements perfectly and delivered a beautiful, functional website.'
    },
    {
        id: 3,
        name: 'Michael Chen',
        position: 'Startup Founder',
        message: 'Sophors helped bring our vision to life. His technical skills in Vue.js and modern web technologies are exceptional.'
    }
]);
</script>
