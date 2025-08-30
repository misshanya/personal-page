<script setup lang="ts">
import { motion } from 'motion-v';

defineProps<{
    title: string
    desc: string
    link: string
}>()
</script>

<template>
    <motion.div class="project"
    :whileHover="{ y: -5 }"
    >
        <div class="info">
            <div class="title">{{ title }}</div>
            <div class="desc">{{ desc }}</div>
        </div>
        <div class="link">
            <a :href="link">More info</a>
        </div>
    </motion.div>
</template>

<style scoped>
.project {
    width: 300px;
    height: 200px;
    background-color: var(--color-background-soft);
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    padding: 20px;

    border-radius: 15px;
    text-align: center;

    box-shadow: 1px 1px 10px rgba(0, 0, 0, 0.2);
}

.title {
    font-size: 25px;
    color: var(--color-heading);
    font-weight: 600;
}

a {
    text-decoration: none;
    color: var(--color-text);
}

.link a {
    padding: 10px;
    border: 2px solid var(--color-border);
    border-radius: 12px;
    transition: all 1s ease;
}

.link a:hover {
    border: 2px solid var(--color-border-hover);
}
</style>