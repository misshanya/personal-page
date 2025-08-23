<script setup lang="ts">
import { motion } from 'motion-v';
</script>

<template>
    <motion.div
        class="about"
    >
        <p>Currently I use <strong>Go</strong> language. I'm trying to write frontend (this page).</p>
    </motion.div>
</template>

<style scoped>
.about {
    width: 100%;
    height: 100vh;

    display: flex;
    justify-content: center;
    align-items: center;

    font-size: 20px;
}

@media (max-width: 1024px) {
    .about {
        padding: 30px;
    }
}

strong {
    color: #8DD8FF;
}
</style>