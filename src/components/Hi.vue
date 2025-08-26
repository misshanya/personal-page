<script setup lang="ts">
import { motion } from 'motion-v';
</script>

<template>
    <div class="me">
        <motion.div class="desc" :initial="{ opacity: 0 }" :animate="{ opacity: 1 }">I'm <b>Mishanya</b> <br> Backend Dev and 16 yo student</motion.div>
        <motion.div class="links" :initial="{ opacity: 0 }" :animate="{ opacity: 1, transition: { duration: 1 } }">
            <motion.a
            href="https://github.com/misshanya"
            :whileHover="{ scale: 1.1 }"
            :whilePress="{ scale: 0.95 }"
            >
                <img src="/github.svg">
            </motion.a>

            <motion.a
            :whileHover="{ scale: 1.1 }"
            :whilePress="{ scale: 0.95 }"
            href="https://t.me/misshanya7"
            >
                <img src="/telegram.svg">
            </motion.a>
        </motion.div>
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
    font-size: 50px;
    text-align: center;
}

.links {
    margin-top: 20px;
    display: flex;
    flex-direction: row;
    gap: 15px;
}

.links img {
    width: 80px;
}

.desc b {
    text-decoration: none;
    color: var(--color-heading);
    font-weight: 600;
    font-size: 75px;
}

@media (max-width: 1024px) {
    .desc {
        font-size: 20px;
    }

    .desc b {
        font-size: 36px;
    }

    .links img {
        width: 40px;
    }
}
</style>