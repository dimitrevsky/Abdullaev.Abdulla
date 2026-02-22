<template>
  <div
    class="card-general-style portfolio-general-style scroll-animation"
    v-for="project in portfolioData"
    :key="project.id"
    :style="{ '--accent-color': project.accentColor }"
  >
    <div>
      <div class="margin-bottom">
        <p class="description-font-general">{{ project.duration }}</p>
      </div>
      <div>
        <h2 class="subtitle-font-general">{{ project.title }}</h2>
      </div>
      <div class="used__stacks">
        <div class="description-font-general stack" v-for="stack in project.stack" :key="stack">
          {{ stack }}
        </div>
      </div>
    </div>

    <div v-if="project.description">
      <p class="normal-font-general">
        {{ project.description }}
      </p>
    </div>

    <div class="normal-font-general">
      <ul>
        <li v-for="tasks in project.tasks" :key="tasks">{{ tasks }}</li>
      </ul>
    </div>

    <div class="portfolio__img">
      <img class="project__img" :src="project.image" :alt="`Image of ${project.title}`" />
      <div class="hover-link">
        <a :href="project.link" target="_blank">
          <p class="normal-font-general">Перейти на сайт</p>
        </a>
      </div>

      <div class="light-animation"></div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  portfolioData: {
    type: Array,
    required: true,
  },
});
</script>

<style scoped>
.used__stacks {
  display: flex;
}

.stack:first-child {
  color: var(--accent-color);
}

.stack:not(:first-of-type)::before {
  content: "•";
  margin: 0 8px;
  color: gray;
  font-size: 15px;
}

ul {
  display: flex;
  flex-direction: column;
  gap: 15px;
}

li::before {
  content: "";
  display: inline-block;
  width: 18px;
  height: 18px;
  margin-right: 5px;
  border: 1px solid var(--accent-color);
  border-radius: 50%;
  vertical-align: sub;
  background: radial-gradient(var(--accent-color) 0, #00000000 72%) no-repeat;
  background-position: center 180%;
  background-size: 140% 80%;
}

.portfolio__img {
  position: relative;
  margin-bottom: -40px;
}

.portfolio__img:hover img {
  filter: brightness(50%);
}

.project__img {
  max-width: 100%;
  min-width: 500px;
  height: auto;
  border-radius: 28px 28px 0 0;
  transition: filter 0.2s linear;
}

.hover-link {
  display: flex;
  opacity: 0;
  gap: 4px;
  align-items: center;
  border-radius: 28px;
  text-wrap: nowrap;
  border: 1px solid #fff;
  background-color: rgb(0, 0, 0);
  padding: 0 20px;
  vertical-align: sub;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  position: absolute;
  transition: all 0.1s linear;
  z-index: 100;
}

.portfolio__img:hover .hover-link {
  opacity: 1;
}

.light-animation {
  position: absolute;
  width: 50%;
  height: 80%;
  top: 10px;
  background-color: var(--accent-color);
  border-radius: 23% 77% 33% 67% / 75% 26% 74% 25%;
  z-index: -100;
  animation: light-animated 14s linear infinite;
}

@keyframes light-animated {
  0% {
    transform: rotate(0deg);
    filter: blur(20px);
  }
  50% {
    transform: rotate(180deg);
    filter: blur(70px);
  }

  100% {
    transform: rotate(360deg);
    filter: blur(20px);
  }
}
@media (max-width: 599px) {
  .portfolio__img {
    position: relative;
    left: 40%;
    bottom: 0;
    transform: translateX(-40%);
  }
}
</style>
