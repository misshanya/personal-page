<script setup lang="ts">
import Project from './Project.vue';
import { motion } from 'motion-v';

const projects = [
    { title: "URL Shortener", desc: "URL Shortener with microservices architecture", link: "https://github.com/misshanya/url-shortener" },
    { title: "Mitter", desc: "My social network", link: "https://github.com/misshanya/mitter" },
    { title: "DNS Switcher", desc: "DNS Server that changes the upstream if current doesn't work", link: "https://github.com/misshanya/dns-switcher" },
    { title: "TGSH", desc: "Telegram bot that provides shell access to your machine without public ip", link: "https://github.com/misshanya/tgsh" },
]
</script>

<template>
    <div class="container">
        <div class="title">My projects</div>
        <div class="projects">
            <motion.div
                v-for="(p, i) in projects"
                :key="i"
                :initial="{ opacity: 0, y: 50 }"
                :animate="{ opacity: 1, y: 0 }"
                :transition="{ delay: i * 0.2 }"
            >
                <Project
                    :title="p.title"
                    :desc="p.desc"
                    :link="p.link"
                />
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

.title {
    margin-bottom: 50px;
    font-size: 70px;
    font-weight: 600;
}

.projects {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 3rem;

}
</style>