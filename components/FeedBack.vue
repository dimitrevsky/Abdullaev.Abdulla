<template>
  <section class="scroll-animation" id="contacts">
    <div>
      <h2 class="title-font-general">Контакты</h2>
    </div>

    <div class="card-general-style">
      <div class="margin-bottom">
        <div>
          <p class="description-font-general">Предпочитаемый вид связи</p>
        </div>
        <div class="feedback__contact">
          <img src="~/assets/img/contact/TelegrammContact.svg" alt="contactImg" />
          <div>
            <h2 class="subtitle-font-general">Telegramm</h2>
            <a href="https://t.me/Dlma_Moroz0v" target="_blank" class="normal-font-general">@Dlma_Moroz0v</a>
          </div>
        </div>
      </div>

      <div>
        <div>
          <p class="description-font-general">Почта</p>
        </div>
        <div class="feedback__contact">
          <img src="~/assets/img/contact/MailContact.svg" alt="contactImg" />
          <div class="mail__contact">
            <p class="normal-font-general">abdulaevabu@mail.ru</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.title-font-general {
  font-size: 56px;
  text-align: center;
  margin-bottom: 24px;
}

.description-font-general {
  margin-bottom: 3px;
}

.feedback__contact {
  display: flex;
  gap: 8px;
  vertical-align: middle;
}

.mail__contact {
  align-self: center;
}
</style>
