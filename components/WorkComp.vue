<template>
    <section class="work">
    <div class="work__container wrapper">
      <h2 class="work__title">Как мы работаем</h2>

      <div class="work__content">
        <div class="work__line">
            <span class="work__line-item">1</span>
            <span class="work__line-item">2</span>
            <span class="work__line-item">3</span>
            <span class="work__line-item">4</span>  
        </div>

        <div class="work__items-container">
          <div class="work__item">
            <h3 class="work__subtitle">Заявка</h3>
            <p class="work__description">
              Вы оставляете заявку на нашем сайте, по e-mail или по телефону
            </p>
          </div>
          <div class="work__item">
            <h3 class="work__subtitle">Утверждение ТЗ</h3>
            <p class="work__description">
              Вы заполняете бриф. Мы проводим анализ информации, утверждаем
              сроки и стоимость
            </p>
          </div>
          <div class="work__item">
            <h3 class="work__subtitle">Заключение договора</h3>
            <p class="work__description">
              Юридически закрепляем все договоренности между нами
            </p>
          </div>
          <div class="work__item">
            <h3 class="work__subtitle">Релиз проекта</h3>
            <p class="work__description">
              Вы становитесь владельцем современного, функционального
              веб-ресурса. способного оставить позади ваших конкурентов
            </p>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<style lang="scss">
  .work__line-item:not(:last-child) {
    margin-right: 23%;
  }
  .work__content {
    display: flex;
    flex-direction: column;
    
  }
  .work__line {
    display: flex;
  }
  .work__line::after {
      position: absolute;
      height: 2px;
      right: 17.5%;
      left: 0;
      background-color: #141b69;;
      content: "";
      top:50%;
  }

  @media screen and (max-width: 1200px) {
    .work__line-item {
      margin-right: 20% !important;
    }
    .work__line::after {
      right: 22%;
    }
  }

  @media screen and (max-width: 960px) {
    .work__line::after {
      position: absolute;
      top: 0;
      width: 2px;
      height: 80%;
      left: 50%;
      content: "";
    }
    .work__line-item {
      margin-right: 0 !important;
      padding: 8px 15px;
      margin-bottom: 75px;
    }
    .work__content {
      flex-direction: row;
      align-items: flex-start;
      & > .work__line {
        display: flex;
        flex-direction: column;
        width: 20%;
        margin: 0;
        margin-top: 20px;
        max-height: 100%;
        height: 100%;
        align-items: center;  
      }
      & .work__items-container {
        flex-direction: column;
        width: 80%;
        
        & .work__item {
          max-width: 100% !important;
        }
      }
    }
  }
  
</style>