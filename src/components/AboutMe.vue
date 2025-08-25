<script setup lang="ts">
import { motion } from 'motion-v';
import { ref } from 'vue';
import { useIntersectionObserver } from '@vueuse/core';

const aboutContainer = ref(null)
const isAboutVisible = ref(false)

useIntersectionObserver(
    aboutContainer,
    ([{ isIntersecting }]) => {
        if (isIntersecting) {
            isAboutVisible.value = true;
        }
    }
)
</script>

<template>
    <div
        class="container"
        ref=aboutContainer
    >
        <div class="about"
        v-if="isAboutVisible"
        >
            <motion.div
            :initial='{ opacity: 0, y: 20 }'
            :animate="{ opacity: 1, y: 0 }"
            :transition="{ duration: 1.5, delay: 0.2, type: 'spring' }"
            >
                <p>I write backend in <img src="/go.svg"> language</p>
            </motion.div>

            <motion.div
            :initial='{ opacity: 0, y: 20 }'
            :animate="{ opacity: 1, y: 0 }"
            :transition="{ duration: 1.5, delay: 0.4, type: 'spring' }"
            >
                <p>I really love complex systems</p>
            </motion.div>

            <motion.div
            :initial='{ opacity: 0, y: 20 }'
            :animate="{ opacity: 1, y: 0 }"
            :transition="{ duration: 1.5, delay: 0.6, type: 'spring' }"
            >
                <p>I use <img src="/linux.svg"> on all of my devices</p>
            </motion.div>
        </div>
    </div>
</template>

<style scoped>
.container {
    width: 100%;
    height: 100vh;

    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}

.about {
    width: 100%;
    height: 100vh;

    display: flex;
    flex-direction: column;
    gap: 30px;
    justify-content: center;
    align-items: center;

    font-size: 40px;
}

.about img {
    width: 50px;
    vertical-align: middle;
}

@media (max-width: 1024px) {
    .about {
        padding: 30px;
        font-size: 20px;
    }
    .about img {
        width: 30px;
    }
}

strong {
    color: #8DD8FF;
}
</style>