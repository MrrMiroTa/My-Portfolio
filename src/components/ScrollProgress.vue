<template>
    <div class="fixed top-0 left-0 w-full h-1 z-50">
        <div 
            class="h-full bg-gradient-to-r from-blue-500 to-cyan-500 transition-all duration-150"
            :style="{ width: scrollWidth + '%' }"
        ></div>
    </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const scrollWidth = ref(0);

const handleScroll = () => {
    const windowHeight = window.innerHeight;
    const documentHeight = document.documentElement.scrollHeight - windowHeight;
    const scrollTop = window.scrollY;
    const scrollPercentage = (scrollTop / documentHeight) * 100;
    scrollWidth.value = Math.min(100, Math.max(0, scrollPercentage));
};

onMounted(() => {
    window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
    window.removeEventListener('scroll', handleScroll);
});
</script>
