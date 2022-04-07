<!-- slider 8 -->
<template>
  <section class="clients">
    <div class="clients__container wrapper">
      <h2 class="clients__title">
        Наши клиенты
      </h2>
      <p class="clients__description">
        Компании, которые доверились нам и остались довольны.
      </p>
    </div>
    <div class="swiper">
      <div class="swiper-wrapper">
        <div class="swiper-slide">
          <img
            class="clients__item"
            src="~/assets/img/clients/enegro.png"
            alt="Энергосбыт Первомайский"
          >
        </div>
        <div class="swiper-slide">
          <img
            class="clients__item"
             src="~/assets/img/clients/eskinvest.png"
            alt="ЭСК Инвест"
          >
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
  @media screen and (max-width: 960px) { 
    .clients {
      padding: 30px 0;
    }
    .clients__container {
      margin-bottom: 0;
    }
    .clients__title {
      font-size: 28px;
      align-self: flex-start;
      margin-bottom: 0;
    }
    .clients__description {
      font-size: 16px;
    }
  }
</style>