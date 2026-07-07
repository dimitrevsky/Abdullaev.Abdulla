<script setup>
import ProjectCard from "./Projects/ProjectCard.vue";

import KometaImg from "~/assets/img/portfolio/KometaImg.svg";
import A2AImg from "~/assets/img/portfolio/A2AImg.svg";
import RoflanMarImg from "~/assets/img/portfolio/RoflanMarImg.svg";
import ArtLebedevImg from "~/assets/img/portfolio/ArtLebedevImg.svg";

const projects = [
  {
    id: 1,
    duration: "Июнь 2024 — Декабрь 2025",
    title: "KometaVPN",
    stack: ["Nuxt 3", "TypeScript"],
    description:
      "Коммерческий VPN-сервис. Работал над сайтом и десктопным приложением — от вёрстки до поддержки в продакшене.",
    tasks: [
      "Разработал сайт сервиса с нуля: вёрстка, анимации, адаптив",
      "Написал десктопное приложение с акцентом на производительность и UX",
      "Поддерживал продукт в продакшене: фиксил баги, внедрял новые фичи по запросу",
    ],
    image: KometaImg,
    accentColor: "#C4C4C4",
    link: "https://kometa-vpn-frontend-redesign.vercel.app/",
  },
  {
    id: 2,
    duration: "Парт-тайм (2 месяца)",
    title: "A2A Global",
    stack: ["Vue 3", "Nuxt 3", "TypeScript"],
    description: "Платформа для альтернативных платежей. Работал в команде разработки над сайтом продукта.",
    tasks: [
      "Разработал сайт продукта с нуля: вёрстка, структура, навигация",
      "Реализовал форму обратной связи с автоматической отправкой данных на почту",
      "Настроил деплой и вывел сайт в продакшен",
    ],
    image: A2AImg,
    accentColor: "#0D72FF",
    link: "https://a2a.global/",
  },
  {
    id: 3,
    duration: "Парт-тайм / Пет-проект",
    title: "RoflanMarket",
    stack: ["Nuxt", "TypeScript"],
    description:
      "Пет-проект в формате маркетплейса. Цель — изучить полный цикл разработки современного веб-приложения: от вёрстки и роутинга до работы с API и много чего",
    tasks: [
      "Разработал структуру приложения на Nuxt 3 с файловым роутингом",
      "Реализовал фильтрацию и сортировку товаров по цене, рейтингу и категории",
      "Реализовал поиск товаров в реальном времени",
      "Создал страницу с подробной информацией о товаре",
      "Настроил динамические маршруты через slug-параметры URL",
      "Реализовал авторизацию через dummyJSON API с хранением сессии в cookie",
    ],
    image: RoflanMarImg,
    accentColor: "#FBBE06",
    link: "https://roflan-market.vercel.app/",
  },
  {
    id: 4,
    duration: "4 дня",
    title: "Генератор форм на основе JSON-схемы",
    stack: ["Nuxt 3", "TypeScript", "Composition API"],
    description:
      "Тестовое задание для студии Артемия Лебедева. Универсальный компонент, который принимает JSON-схему и автоматически генерирует валидируемую форму с поддержкой различных типов полей.",
    tasks: [
      "Реализовал динамическую генерацию полей формы на основе JSON-схемы",
      "Добавил поддержку типов полей: text, email, password, select, checkbox",
      "Настроил двустороннее связывание данных через v-model",
      "Реализовал валидацию полей: required, minLength, pattern",
      "Выстроил компонентную архитектуру с разделением ответственности",
      "Покрыл всю логику TypeScript-типизацией",
    ],
    image: ArtLebedevImg,
    accentColor: "#EC2227",
    link: "https://art-lebedev-studio-test-vue3-mv6a8ldai-dmitryxmorozovs-projects.vercel.app/",
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

<!--
 копипаста, быстро добавить новую работу:

 {
    id: ,
    duration: "",
    title: "",
    stack: ["", ""],
    description:
      "",
    tasks: [
      "",
      "",
    ],
    image: ,
    accentColor: "#",
    link: "",
  },

-->
