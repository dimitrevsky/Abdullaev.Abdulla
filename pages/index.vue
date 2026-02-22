<template>
  <Navigation />
  <main>
    <Title />
    <AboutMe />
    <Stack />
    <Portfolio />
    <FeedBack />
  </main>
</template>

<script setup>
import Title from "~/components/Title.vue";
import AboutMe from "~/components/AboutMe.vue";
import Stack from "~/components/Stack.vue";
import Portfolio from "~/components/Portfolio.vue";
import FeedBack from "~/components/FeedBack.vue";
import Navigation from "~/components/Navigation.vue";
</script>

<style scoped>
main {
  display: flex;
  flex-direction: column;
  gap: 80px;
  max-width: 835px;
  padding: 0 16px;
  padding-bottom: 300px;
  padding-top: 100px;
  margin: 0 auto;
}
</style>
