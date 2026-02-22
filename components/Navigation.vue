<template>
  <nav class="nav">
    <div>
      <ul class="nav__wrapper">
        <li
          class="nav__option normal-font-general"
          @click.prevent="scrollToSection('about')"
          :class="{ active: activeSection === 'about' }"
        >
          <a href="#about"> О себе </a>
        </li>

        <li
          class="nav__option normal-font-general"
          @click.prevent="scrollToSection('portfolio')"
          :class="{ active: activeSection === 'portfolio' }"
        >
          <a href="#portfolio"> Портфолио</a>
        </li>

        <li
          class="nav__option normal-font-general"
          @click.prevent="scrollToSection('contacts')"
          :class="{ active: activeSection === 'contacts' }"
        >
          <a href="#contacts"> Контакты </a>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script setup>
import { ref, onMounted } from "vue";
import { useIntersectionObserver } from "@vueuse/core";

const activeSection = ref("about");

function scrollToSection(id) {
  const element = document.getElementById(id);
  if (element) {
    window.scrollTo({
      top: element.offsetTop - 140,
      behavior: "smooth",
    });
  }
}

function observeSection() {
  const sections = document.querySelectorAll("section");

  if (sections.length > 0) {
    sections.forEach((section) => {
      useIntersectionObserver(
        section,
        ([entry]) => {
          if (entry.isIntersecting) {
            activeSection.value = entry.target.id;
          }
        },
        {
          threshold: 0.2,
        }
      );
    });
  }
}

onMounted(observeSection);
</script>

<style scoped>
.nav {
  position: sticky;
  top: 10px;
  margin: 30px auto;
  max-width: 356px;
  text-wrap: nowrap;
  background-color: var(--card-background-color);
  border-radius: 32px;
  z-index: 1000;
  border: 2px solid white;
  padding: 4px;
}

.nav__wrapper {
  display: flex;
  justify-content: space-between;
}

.nav__option {
  padding: 12px;
  cursor: pointer;
  border-radius: 32px;
  transition: background-color 0.2s linear;
}

.nav__option:hover {
  background-color: #252525;
}

.nav__option.active {
  background-color: white;
  transition: background-color 0.7s linear;
}

.nav__option.active > a {
  color: black;
}

a {
  text-decoration: none;
}
</style>
