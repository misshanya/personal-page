<script setup lang="ts">
import { motion } from 'motion-v';
</script>

<template>
    <div class="me">
        <motion.div class="desc" :initial="{ scale: 0 }" :animate="{ scale: 1 }">I'm <a href="https://github.com/misshanya">Mishanya</a> <br> Backend Dev and 16 yo student</motion.div>
    </div>
</template>

<style scoped>
.me {
    width: 100%;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.desc {
    font-size: 30px;
    text-align: center;
}

@media (max-width: 1024px) {
    .desc {
        font-size: 20px;
    }

    .desc a {
        font-size: 36px;
    }
}

.desc a {
    text-decoration: none;
    color: var(--color-heading);
    font-weight: 600;
    font-size: 55px;
}
</style>