<template lang="html">
    <div class="relative py-24 overflow-hidden bg-linear-to-r from-blue-900/50 to-cyan-900/50" id="educations">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16" data-aos="fade-up">
                <h2 class="text-4xl font-bold text-white mb-6 tracking-tight">
                    <span class="text-transparent bg-clip-text bg-linear-to-r from-blue-500 to-cyan-500">My Education</span>
                </h2>
                <p class="mt-4 text-blue-300 max-w-3xl mx-auto text-lg leading-relaxed">
                    Here is a summary of my educational background, highlighting the institutions I've attended and the qualifications I've earned.
                </p>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8" data-aos="fade-up" data-aos-delay="200">
                <div v-for="(education, index) in educations" :key="education.id" :data-aos="'fade-up'" :data-aos-delay="index * 100">
                    <div class="group relative bg-gray-800 rounded-2xl border border-blue-500/20 shadow-lg hover:shadow-2xl transition-all duration-500 hover:-translate-y-2">
                        <div class="absolute inset-0 bg-linear-to-r from-blue-500/10 to-cyan-500/10 rounded-2xl opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                        <div class="relative p-8">
                            <h3 class="text-xl font-bold text-white mb-4 group-hover:text-cyan-300 transition-colors duration-300">{{ education.degree }}</h3>
                            <p class="text-blue-300 leading-relaxed mb-2">{{ education.institution }}</p>
                            <p class="text-blue-400 italic">{{ education.year }}</p>
                        </div>
                    </div>
                </div>
                </div>


        </div>
        
    </div>
</template>
<script>
import { ref } from 'vue';
export default {
    setup() {
        const educations = ref([
            {
                id: 1,
                degree: 'Bachelor of Science in Computer Science',
                institution: 'Royal University of Phnom Penh',
                year: '2022 - 2025'
            },
            {
                id: 2,
                degree: ' High School Diploma ',
                institution: 'Stueng Sen High School',
                year: '2014 - 2021'
            }
            
        ]);
        return { educations };
    }
}
</script>
<style lang="">
    
</style>