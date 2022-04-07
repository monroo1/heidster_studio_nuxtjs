<!-- slider 8 -->
<template>
  <section class="feedback">
    <div class="feedback__container">
      <h2 class="feedback__title">
        Отзывы
      </h2>
    </div>

    <div class="swiper-wrapper">

      <div class="swiper-slide">
        <div class="feedback__container">
          <div class="feedback__slide">
            <img
              src="~/assets/img/profile-logo.jpg"
              alt="logo.jpg"
              class="feedback__slide-logo"
            >
            <div class="feedback__slide-container">
              <p class="feedback__review">
                I think if you do something and it turns out pretty good, then
                you should go do something else wonderful, not dwell on it for
                too long.
              </p>
              <p class="feedback__author">
                Samuel Willson
              </p>
              <p class="feedback__working">
                Creative director in
                <span class="feedback__working-span">DD agency</span>
              </p>
            </div>
          </div>
        </div>
      </div>
      
    </div>
  </section>
</template>

<script>
export default ({
  data() {
    return {
      feedbackSlider: {
        title: "Отзывы",
        blocks: [
          {
            author: "Sarah Lewin",
            authorPosition: "Project manager in Pixels",
            text: "Все понравилось. Ребята из Heidster Studio выполнили работу по разработке сайта и логотипа быстро и в срок, четко по ТЗ. Все разговоры по делу, без лишней суеты. Ни разу не пожалел, что обратился к ним. ",
            img: "profile-logo"
          },
          {
            author: "Sarah Lewin",
            authorPosition: "Project manager in Pixels",
            text: "Все понравилось. Ребята из Heidster Studio выполнили работу по разработке сайта и логотипа быстро и в срок, четко по ТЗ. Все разговоры по делу, без лишней суеты. Ни разу не пожалел, что обратился к ним. ",
            img: "profile-logo"
          },
          {
            author: "Sarah Lewin",
            authorPosition: "Project manager in Pixels",
            text: "Все понравилось. Ребята из Heidster Studio выполнили работу по разработке сайта и логотипа быстро и в срок, четко по ТЗ. Все разговоры по делу, без лишней суеты. Ни разу не пожалел, что обратился к ним. ",
            img: "profile-logo"
          }
        ]
      }
    }
  },
})
</script>

<style lang="scss">
  @media screen and (max-width: 960px) {
    .feedback__title {
      font-size: 28px;
      margin-bottom: 30px;
    }
  }
</style>