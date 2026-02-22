<script setup>
import ProjectCard from "./Projects/ProjectCard.vue";

import KometaImg from "~/assets/img/portfolio/KometaImg.svg";
import A2AImg from "~/assets/img/portfolio/A2AImg.svg";
import RoflanMarImg from "~/assets/img/portfolio/RoflanMarImg.svg";

const projects = [
  {
    id: 1,
    duration: "С июня 2024 года по настоящее время",
    title: "KometaVPN",
    stack: ["Vue", "Nuxt"],
    description: "",
    tasks: [
      "Разработал современный сайт с интуитивным интерфейсом и стильным дизайном, подчёркивающим бренд",
      "Написал десктопное приложение для ПК с фокусом на стабильность, производительность и комфорт пользователей",
      "Постоянно улучшаю продукт: внедряю новые функции, оптимизирую работу и быстро реагирую на запросы",
    ],
    image: KometaImg,
    accentColor: "#27DF8D",
    link: "https://kometa-vpn-frontend-redesign.vercel.app/",
  },
  {
    id: 2,
    duration: "Парт-тайм проект",
    title: "A2A Global",
    stack: ["Vue", "Nuxt"],
    description: " A2A Global — платформа для альтернативных платежей, где я был частью команды разработки",
    tasks: [
      "Создал функциональный и стильный сайт с простым доступом к информации о продукте",
      "Реализовал форму обратной связи с автоматической отправкой данных, ускорив коммуникацию с клиентами",
      "Провёл деплой и настройку сайта для стабильной работы",
    ],
    image: A2AImg,
    accentColor: "#0D72FF",
    link: "https://a2a.global/",
  },
  {
    id: 3,
    duration: "пет-проект",
    title: "RoflanMarket",
    stack: ["Nuxt"],
    description:
      "Пет-проект по созданию интернет-магазина, в котором я изучаю, как реализовать функционал и дизайн веб-приложения, концепт приложения я взял в качестве Маркет плейса, так как подобные проекты дают максимум опыта в изучении современных веб-технологий",
    tasks: [],
    image: RoflanMarImg,
    accentColor: "#FBBE06",
    link: "https://roflan-market.vercel.app/",
  },
];
</script>

<template>
  <section class="portfolio" id="portfolio">
    <ProjectCard :portfolio-data="projects" />
  </section>
</template>

<style scoped>
.portfolio {
  display: flex;
  flex-direction: column;
  gap: 20px;
  scroll-margin-top: 100px;
}
</style>
