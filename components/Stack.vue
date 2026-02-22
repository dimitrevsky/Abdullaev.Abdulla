<template>
  <section class="scroll-animation" id="portfolio">
    <div class="margin-bottom">
      <h1 class="title-font-general">С чем работал</h1>
    </div>
    <div class="stack__wrapper card-general-style">
      <div class="stack__container">
        <div class="stack__title">
          <img src="~/assets/img/stacks/VueStack.png" alt="Vue" />
          <h2 class="subtitle-font-general">Vue 2/3</h2>
        </div>
        <div>
          <p class="description-font-general">разработка проектов</p>
        </div>
      </div>

      <div class="stack__container">
        <div class="stack__title">
          <img src="~/assets/img/stacks/GithubStack.png" alt="GitHub" />
          <h2 class="subtitle-font-general">Github/Git</h2>
        </div>
        <div>
          <p class="description-font-general">Управление версиями</p>
        </div>
      </div>

      <div class="stack__container">
        <div class="stack__title">
          <img src="~/assets/img/stacks/FigmaStack.png" alt="Figma" />
          <h2 class="subtitle-font-general">Figma</h2>
        </div>
        <div>
          <p class="description-font-general">Работа с макетами</p>
        </div>
      </div>

      <div class="stack__container">
        <div class="stack__title">
          <img src="~/assets/img/stacks/VercelStack.png" alt="Vercel" />
          <h2 class="subtitle-font-general">Vercel</h2>
        </div>
        <div>
          <p class="description-font-general">Деплой своих страниц</p>
        </div>
      </div>

      <div class="stack__container">
        <div class="stack__title">
          <img src="~/assets/img/stacks/GodaddyStack.png" alt="Godaddy" />
          <h2 class="subtitle-font-general">GoDaddy</h2>
        </div>
        <div>
          <p class="description-font-general">Деплой проектов</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.stack__wrapper {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
  row-gap: 32px;
  grid-auto-flow: row;
}

.stack__container {
  display: flex;
  flex-direction: column;
  max-width: 273px;
  gap: 12px;
}

.stack__title {
  display: flex;
  align-content: center;
  align-items: center;
  gap: 8px;
}

img {
  max-width: 20px;
  height: 20px;
}
</style>
