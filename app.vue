<template>
  <div>
    <NuxtPage />
  </div>
</template>

<script setup>
import "./assets/styles.css";

useHead({
  title: "Abdullaev Abdulla",
  meta: [
    { property: 'og:title', content: 'Abdullaev Abdulla' },
    { property: 'og:description', content: "Меня зовут Абдулла и я фронтенд-разработчик. Несмотря на небольшой промежуток времени, я уже имею опыт работы с реальными проектами, включая создание социальной платформы и также разработка VPN-сервиса", },
    { property: 'og:image', content: 'https://abdullaev-portfolio.vercel.app/img/OgImg.png?v=2' },
    { property: 'og:type', content: 'website' },
    { name: 'twitter:card', content: 'summary_large_image' },
    { name: 'twitter:image', content: 'https://abdullaev-portfolio.vercel.app/img/OgImg.png' },
  ],
});
</script>
