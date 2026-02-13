<template lang="html">
    <div class="relative py-24 overflow-hidden bg-linear-to-r from-blue-900/50 to-cyan-900/50" id="skills">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16" data-aos="fade-up">
                <h2 class="text-4xl font-bold text-white mb-6 tracking-tight">
                    <span class="text-transparent bg-clip-text bg-linear-to-r from-blue-500 to-cyan-500">My Skills</span>
                </h2>
                <p class="mt-4 text-blue-300 max-w-3xl mx-auto text-lg leading-relaxed">
                    A comprehensive overview of the technologies and tools I use to bring ideas to life.
                </p>
            </div>
            
            <!-- Frontend Skills -->
            <div class="mb-12" data-aos="fade-up" data-aos-delay="100">
                <h3 class="text-2xl font-bold text-white mb-6 flex items-center">
                    <span class="mr-3 text-cyan-400">&#60;/&#62;</span> Frontend
                </h3>
                <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-6 gap-6">
                    <div v-for="skill in frontendSkills" :key="skill.name" 
                         class="group bg-gray-800 rounded-xl p-6 text-center border border-blue-500/20 hover:border-cyan-400/50 hover:shadow-lg hover:shadow-cyan-500/10 transition-all duration-300 hover:-translate-y-1">
                        <div class="text-5xl mb-3 group-hover:scale-110 transition-transform duration-300">{{ skill.icon }}</div>
                        <h4 class="text-white font-medium">{{ skill.name }}</h4>
                        <div class="w-full bg-gray-700 rounded-full h-2 mt-3">
                            <div class="bg-linear-to-r from-blue-500 to-cyan-500 h-2 rounded-full transition-all duration-500" :style="{ width: skill.level + '%' }"></div>
                        </div>
                        <span class="text-xs text-gray-400 mt-1">{{ skill.level }}%</span>
                    </div>
                </div>
            </div>

            <!-- Backend Skills -->
            <div class="mb-12" data-aos="fade-up" data-aos-delay="200">
                <h3 class="text-2xl font-bold text-white mb-6 flex items-center">
                    <span class="mr-3 text-cyan-400">&#9881;</span> Backend
                </h3>
                <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-6 gap-6">
                    <div v-for="skill in backendSkills" :key="skill.name" 
                         class="group bg-gray-800 rounded-xl p-6 text-center border border-blue-500/20 hover:border-cyan-400/50 hover:shadow-lg hover:shadow-cyan-500/10 transition-all duration-300 hover:-translate-y-1">
                        <div class="text-5xl mb-3 group-hover:scale-110 transition-transform duration-300">{{ skill.icon }}</div>
                        <h4 class="text-white font-medium">{{ skill.name }}</h4>
                        <div class="w-full bg-gray-700 rounded-full h-2 mt-3">
                            <div class="bg-linear-to-r from-blue-500 to-cyan-500 h-2 rounded-full transition-all duration-500" :style="{ width: skill.level + '%' }"></div>
                        </div>
                        <span class="text-xs text-gray-400 mt-1">{{ skill.level }}%</span>
                    </div>
                </div>
            </div>

            <!-- Database Skills -->
            <div class="mb-12" data-aos="fade-up" data-aos-delay="300">
                <h3 class="text-2xl font-bold text-white mb-6 flex items-center">
                    <span class="mr-3 text-cyan-400">&#128451;</span> Database
                </h3>
                <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
                    <div v-for="skill in databaseSkills" :key="skill.name" 
                         class="group bg-gray-800 rounded-xl p-6 text-center border border-blue-500/20 hover:border-cyan-400/50 hover:shadow-lg hover:shadow-cyan-500/10 transition-all duration-300 hover:-translate-y-1">
                        <div class="text-5xl mb-3 group-hover:scale-110 transition-transform duration-300">{{ skill.icon }}</div>
                        <h4 class="text-white font-medium">{{ skill.name }}</h4>
                        <div class="w-full bg-gray-700 rounded-full h-2 mt-3">
                            <div class="bg-linear-to-r from-blue-500 to-cyan-500 h-2 rounded-full transition-all duration-500" :style="{ width: skill.level + '%' }"></div>
                        </div>
                        <span class="text-xs text-gray-400 mt-1">{{ skill.level }}%</span>
                    </div>
                </div>
            </div>

            <!-- Tools & Others -->
            <div data-aos="fade-up" data-aos-delay="400">
                <h3 class="text-2xl font-bold text-white mb-6 flex items-center">
                    <span class="mr-3 text-cyan-400">&#128295;</span> Tools & Others
                </h3>
                <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-5 gap-6">
                    <div v-for="skill in toolSkills" :key="skill.name" 
                         class="group bg-gray-800 rounded-xl p-6 text-center border border-blue-500/20 hover:border-cyan-400/50 hover:shadow-lg hover:shadow-cyan-500/10 transition-all duration-300 hover:-translate-y-1">
                        <div class="text-5xl mb-3 group-hover:scale-110 transition-transform duration-300">{{ skill.icon }}</div>
                        <h4 class="text-white font-medium">{{ skill.name }}</h4>
                        <div class="w-full bg-gray-700 rounded-full h-2 mt-3">
                            <div class="bg-linear-to-r from-blue-500 to-cyan-500 h-2 rounded-full transition-all duration-500" :style="{ width: skill.level + '%' }"></div>
                        </div>
                        <span class="text-xs text-gray-400 mt-1">{{ skill.level }}%</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            frontendSkills: [
                { name: 'HTML5', icon: '&#128187;', level: 95 },
                { name: 'CSS3', icon: '&#127912;', level: 90 },
                { name: 'JavaScript', icon: '&#128187;', level: 85 },
                { name: 'Vue.js', icon: '&#128187;', level: 80 },
                { name: 'React', icon: '&#128187;', level: 75 },
                { name: 'Tailwind CSS', icon: '&#128187;', level: 85 }
            ],
            backendSkills: [
                { name: 'PHP', icon: '&#128187;', level: 80 },
                { name: 'Laravel', icon: '&#128187;', level: 75 },
                { name: 'Node.js', icon: '&#128187;', level: 70 },
                { name: 'Express', icon: '&#128187;', level: 65 },
                { name: 'Python', icon: '&#128187;', level: 60 }
            ],
            databaseSkills: [
                { name: 'MySQL', icon: '&#128451;', level: 85 },
                { name: 'MongoDB', icon: '&#128451;', level: 70 },
                { name: 'Firebase', icon: '&#128451;', level: 75 }
            ],
            toolSkills: [
                { name: 'Git', icon: '&#128295;', level: 85 },
                { name: 'GitHub', icon: '&#128295;', level: 80 },
                { name: 'VS Code', icon: '&#128295;', level: 95 },
                { name: 'Postman', icon: '&#128295;', level: 75 },
                { name: 'Figma', icon: '&#128295;', level: 65 }
            ]
        }
    }
}
</script>
