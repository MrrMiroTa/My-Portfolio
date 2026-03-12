<template>
    <span class="typewriter">
        <span ref="text" class="typing-text"></span>
        <span class="cursor">|</span>
    </span>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const props = defineProps({
    text: {
        type: String,
        default: ''
    },
    speed: {
        type: Number,
        default: 100
    }
});

const text = ref('');
const textRef = ref(null);
let timeout = null;

const typeWriter = (i = 0) => {
    if (i < props.text.length) {
        text.value = props.text.substring(0, i + 1);
        timeout = setTimeout(() => {
            typeWriter(i + 1);
        }, props.speed);
    }
};

const resetAndType = () => {
    text.value = '';
    setTimeout(() => {
        typeWriter(0);
    }, 500);
};

onMounted(() => {
    typeWriter(0);
    setInterval(resetAndType, (props.text.length * props.speed) + 2000);
});

onUnmounted(() => {
    if (timeout) clearTimeout(timeout);
});
</script>

<style scoped>
.typewriter {
    display: inline-block;
}

.cursor {
    display: inline-block;
    color: #60a5fa;
    animation: blink 1s infinite;
    font-weight: bold;
}

@keyframes blink {
    0%, 50% { opacity: 1; }
    51%, 100% { opacity: 0; }
}
</style>
