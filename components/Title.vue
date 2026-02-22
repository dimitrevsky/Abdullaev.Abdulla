<template>
  <section class="tilte__wrapper" id="about">
    <div>
      <p class="tilte__wrapper__name">
        Абдуллаев <br />
        Абдулла
      </p>
      <p class="tilte__wrapper__job_title">Front-end Developer</p>
    </div>
    <div>
      <video autoplay playsinline loop muted width="260px" height="auto">
        <source src="../assets/video/VideoAbstract.mp4" type="video/mp4" />
      </video>
    </div>
  </section>
</template>

<style scoped>
.tilte__wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
}

.tilte__wrapper__job_title {
  font-size: 32px;
  font-weight: 600;
}

.tilte__wrapper__name {
  font-size: 100px;
  font-family: var(--ff-title-text);
  font-weight: 800;
  margin-bottom: 17px;
  background-image: linear-gradient(#ffffff 0%, #999999 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  line-height: 95%;
  padding-bottom: 0.1em;
  overflow: visible;
  letter-spacing: -3px;
}

@media (max-width: 492px) {
  .tilte__wrapper__job_title {
    font-size: 24px;
  }

  .tilte__wrapper__name {
    font-size: 64px;
  }
}
</style>
