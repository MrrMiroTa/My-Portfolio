<template>
    <section class="relative w-full overflow-hidden min-h-screen flex items-center justify-center">
        <div class="w-full px-5 sm:px-8 md:px-12 lg:px-8 max-w-5xl lg:max-w-7xl mx-auto relative z-10">
            <div class="grid lg:grid-cols-2 gap-10 xl:gap-14 items-center">
                <div class="flex flex-col md:mt-0 mt-20 justify-center">
                    <div class="text-white lg:text-left" data-aos="fade-up" data-aos-delay="200">
                        <h1 class="text-white font-bold text-4xl md:text-5xl lg:text-6xl">Hello 👋 , I'm
                            <span
                                class="text-transparent bg-clip-text bg-gradient-to-r from-blue-500 to-cyan-500">Sophors</span>
                        </h1>
                        <p class="mt-6 text-blue-200 text-lg md:text-xl lg:text-xl leading-relaxed" data-aos="fade-up"
                            data-aos-delay="400">A passionate
                            <span
                                class="text-transparent bg-clip-text bg-gradient-to-r from-blue-400 to-cyan-400 font-semibold">Web
                                Developer</span>
                            crafting seamless web experiences with modern technologies.
                        </p>
                    </div>
                    <div class="flex items-center gap-3 pt-8 flex-col sm:flex-row" data-aos="fade-up"
                        data-aos-delay="600">
                        <a href="#projects"
                            class="border-2 border-blue-400 px-6 md:px-10 py-4 bg-blue-400 rounded-xl relative group w-full sm:flex-1 flex justify-center whitespace-nowrap hover:bg-blue-700 transition-all duration-300 font-medium text-white text-center text-sm md:text-base">
                            View Projects
                        </a>
                        <a href="#contact"
                            class="border-2 bg-blue-500 border-blue-400 px-6 md:px-10 py-4 rounded-xl relative group w-full sm:flex-1 flex justify-center items-center whitespace-nowrap transition-all duration-300 hover:bg-blue-400 hover:shadow-lg hover:shadow-blue-500/30 hover:scale-105 font-medium text-white gap-2 text-center text-sm md:text-base">
                            Contact Me
                            <ArrowRightIcon class="w-5 h-5 group-hover:translate-x-1 text-white transition-transform" />
                        </a>
                        <a href="/CV_DoeunSophors.pdf" download="CV_DoeunSophors.pdf"
                            class="border-2 border-blue-400 bg-gradient-to-r from-blue-500 to-cyan-500 px-6 md:px-10 py-4 rounded-xl relative group w-full sm:flex-1 flex justify-center items-center whitespace-nowrap hover:from-blue-600 hover:to-cyan-600 hover:shadow-lg hover:shadow-blue-500/30 hover:scale-105 transition-all duration-300 font-medium text-white gap-2 text-center text-sm md:text-base">
                            <ArrowDownTrayIcon class="w-5 h-5 group-hover:translate-y-1 text-white transition-transform" />
                            <span>Download CV</span>
                        </a>
                    </div>
                    <div class="flex items-center justify-center lg:justify-start gap-4 lg:gap-8 pt-12"
                        data-aos="fade-up" data-aos-delay="400">
                        <div class="text-center px-4 py-2 bg-blue-500/10 rounded-lg backdrop-blur-sm border border-blue-500/20">
                            <div class="text-2xl md:text-3xl font-bold text-blue-400">10+</div>
                            <div class="text-blue-200 text-sm">Projects</div>
                        </div>
                        <div class="text-center px-4 py-2 bg-blue-500/10 rounded-lg backdrop-blur-sm border border-blue-500/20">
                            <div class="text-2xl md:text-3xl font-bold text-blue-400">5+</div>
                            <div class="text-blue-200 text-sm">Clients</div>
                        </div>
                        <div class="text-center px-4 py-2 bg-blue-500/10 rounded-lg backdrop-blur-sm border border-blue-500/20">
                            <div class="text-2xl md:text-3xl font-bold text-blue-400">2+</div>
                            <div class="text-blue-200 text-sm">Years Exp.</div>
                        </div>
                    </div>
                </div>
                <div class="lg:h-full flex justify-center lg:justify-end" data-aos="fade-left" data-aos-delay="800">
                    <div class="relative w-full max-w-md lg:max-w-lg">
                        <div class="absolute inset-0 bg-gradient-to-r from-blue-500 to-cyan-500 rounded-[50%_40%_50%_40%/60%_60%_40%_40%] blur-2xl opacity-30"></div>
                        <div class="relative z-10 bg-gradient-to-r from-blue-300 to-cyan-500 shadow-2xl rounded-[50%_40%_50%_40%/60%_60%_40%_40%] p-3 backdrop-blur-sm border border-blue-500/30">
                            <img src="../assets/card.jpg" alt="Sophors - Web Developer" 
                                class="w-full h-auto rounded-[50%_40%_50%_40%/60%_60%_40%_40%] object-cover shadow-inner" />
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
<script setup>
import { ArrowRightIcon, ArrowDownTrayIcon } from '@heroicons/vue/16/solid';
</script>
<style></style>
