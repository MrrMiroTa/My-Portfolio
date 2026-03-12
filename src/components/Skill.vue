<template lang="html">
    <div class="relative py-24 overflow-hidden bg-gradient-to-r from-blue-900/50 to-cyan-900/50" id="skills">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16" data-aos="fade-up">
                <h2 class="text-4xl font-bold text-white mb-6 tracking-tight">
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-500 to-cyan-500">My Skills</span>
                </h2>
                <p class="mt-4 text-blue-300 max-w-3xl mx-auto text-lg leading-relaxed">
                    A comprehensive overview of the technologies and tools I use to bring ideas to life.
                </p>
            </div>
            
            <!-- Frontend Skills -->
            <div class="mb-12" data-aos="fade-up" data-aos-delay="100">
                <h3 class="text-2xl font-bold text-white mb-6 flex items-center">
                    <span class="mr-3 text-cyan-400 text-2xl">&#60;/&#62;</span> Frontend
                </h3>
                <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-6 gap-4 md:gap-6">
                    <div v-for="skill in frontendSkills" :key="skill.name" 
                         class="group bg-gray-800/80 backdrop-blur-sm rounded-xl p-4 md:p-6 text-center border border-blue-500/20 hover:border-cyan-400/50 hover:shadow-lg hover:shadow-cyan-500/10 transition-all duration-300 hover:-translate-y-1">
                        <div class="flex justify-center mb-2 md:mb-3">
                            <img :src="skill.icon" :alt="skill.name" class="w-12 h-12 md:w-14 md:h-14 object-contain group-hover:scale-110 transition-transform duration-300">
                        </div>
                        <h4 class="text-white font-medium text-sm md:text-base">{{ skill.name }}</h4>
                        <div class="w-full bg-gray-700/50 rounded-full h-1.5 md:h-2 mt-2 md:mt-3 overflow-hidden">
                            <div class="bg-gradient-to-r from-blue-500 to-cyan-500 h-full rounded-full transition-all duration-500" :style="{ width: skill.level + '%' }"></div>
                        </div>
                        <span class="text-xs text-gray-400 mt-1">{{ skill.level }}%</span>
                    </div>
                </div>
            </div>

            <!-- Backend Skills -->
            <div class="mb-12" data-aos="fade-up" data-aos-delay="200">
                <h3 class="text-2xl font-bold text-white mb-6 flex items-center">
                    <span class="mr-3 text-cyan-400 text-2xl">&#9881;</span> Backend
                </h3>
                <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-6 gap-4 md:gap-6">
                    <div v-for="skill in backendSkills" :key="skill.name" 
                         class="group bg-gray-800/80 backdrop-blur-sm rounded-xl p-4 md:p-6 text-center border border-blue-500/20 hover:border-cyan-400/50 hover:shadow-lg hover:shadow-cyan-500/10 transition-all duration-300 hover:-translate-y-1">
                        <div class="flex justify-center mb-2 md:mb-3">
                            <img :src="skill.icon" :alt="skill.name" class="w-12 h-12 md:w-14 md:h-14 object-contain group-hover:scale-110 transition-transform duration-300">
                        </div>
                        <h4 class="text-white font-medium text-sm md:text-base">{{ skill.name }}</h4>
                        <div class="w-full bg-gray-700/50 rounded-full h-1.5 md:h-2 mt-2 md:mt-3 overflow-hidden">
                            <div class="bg-gradient-to-r from-blue-500 to-cyan-500 h-full rounded-full transition-all duration-500" :style="{ width: skill.level + '%' }"></div>
                        </div>
                        <span class="text-xs text-gray-400 mt-1">{{ skill.level }}%</span>
                    </div>
                </div>
            </div>

            <!-- Database Skills -->
            <div class="mb-12" data-aos="fade-up" data-aos-delay="300">
                <h3 class="text-2xl font-bold text-white mb-6 flex items-center">
                    <span class="mr-3 text-cyan-400 text-2xl">&#128451;</span> Database
                </h3>
                <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4 md:gap-6">
                    <div v-for="skill in databaseSkills" :key="skill.name" 
                         class="group bg-gray-800/80 backdrop-blur-sm rounded-xl p-4 md:p-6 text-center border border-blue-500/20 hover:border-cyan-400/50 hover:shadow-lg hover:shadow-cyan-500/10 transition-all duration-300 hover:-translate-y-1">
                        <div class="flex justify-center mb-2 md:mb-3">
                            <img :src="skill.icon" :alt="skill.name" class="w-12 h-12 md:w-14 md:h-14 object-contain group-hover:scale-110 transition-transform duration-300">
                        </div>
                        <h4 class="text-white font-medium text-sm md:text-base">{{ skill.name }}</h4>
                        <div class="w-full bg-gray-700/50 rounded-full h-1.5 md:h-2 mt-2 md:mt-3 overflow-hidden">
                            <div class="bg-gradient-to-r from-blue-500 to-cyan-500 h-full rounded-full transition-all duration-500" :style="{ width: skill.level + '%' }"></div>
                        </div>
                        <span class="text-xs text-gray-400 mt-1">{{ skill.level }}%</span>
                    </div>
                </div>
            </div>

            <!-- Tools & Others -->
            <div data-aos="fade-up" data-aos-delay="400">
                <h3 class="text-2xl font-bold text-white mb-6 flex items-center">
                    <span class="mr-3 text-cyan-400 text-2xl">&#128295;</span> Tools & Others
                </h3>
                <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-5 gap-4 md:gap-6">
                    <div v-for="skill in toolSkills" :key="skill.name" 
                         class="group bg-gray-800/80 backdrop-blur-sm rounded-xl p-4 md:p-6 text-center border border-blue-500/20 hover:border-cyan-400/50 hover:shadow-lg hover:shadow-cyan-500/10 transition-all duration-300 hover:-translate-y-1">
                        <div class="flex justify-center mb-2 md:mb-3">
                            <img :src="skill.icon" :alt="skill.name" class="w-12 h-12 md:w-14 md:h-14 object-contain group-hover:scale-110 transition-transform duration-300">
                        </div>
                        <h4 class="text-white font-medium text-sm md:text-base">{{ skill.name }}</h4>
                        <div class="w-full bg-gray-700/50 rounded-full h-1.5 md:h-2 mt-2 md:mt-3 overflow-hidden">
                            <div class="bg-gradient-to-r from-blue-500 to-cyan-500 h-full rounded-full transition-all duration-500" :style="{ width: skill.level + '%' }"></div>
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
                { name: 'HTML5', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg', level: 95 },
                { name: 'CSS3', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg', level: 90 },
                { name: 'JavaScript', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg', level: 85 },
                { name: 'Vue.js', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vuejs/vuejs-original.svg', level: 80 },
                { name: 'React', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg', level: 75 },
                { name: 'Tailwind', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-original.svg', level: 85 }
            ],
            backendSkills: [
                { name: 'PHP', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg', level: 80 },
                { name: 'Laravel', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/laravel/laravel-original.svg', level: 75 },
                { name: 'Node.js', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg', level: 70 },
                { name: 'Express', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/express/express-original.svg', level: 65 },
                { name: 'Python', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg', level: 60 }
            ],
            databaseSkills: [
                { name: 'MySQL', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg', level: 85 },
                { name: 'MongoDB', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg', level: 70 },
                { name: 'Firebase', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/firebase/firebase-plain.svg', level: 75 }
            ],
            toolSkills: [
                { name: 'Git', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg', level: 85 },
                { name: 'GitHub', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg', level: 80 },
                { name: 'VS Code', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg', level: 95 },
                { name: 'Postman', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postman/postman-original.svg', level: 75 },
                { name: 'Figma', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/figma/figma-original.svg', level: 65 }
            ]
        }
    }
}
</script>
