<!-- slider 8 -->
<template>
  <div>
    <section class="project" style="overflow: hidden">
      <div class="project__container">
        <div class="wrapper">
          <h2 class="project__title">Разработка сайтов</h2>
          <div class="line" style="width: 200px" />
          <p class="project__desription">
            Мы проводим глубокий анализ каждого проекта. Используем комплексный
            подход к проектированию прототипов и программной разработке,
            учитывающий особенности сферы деятельности вашего бизнеса.
          </p>
        </div>
      </div>

      <div class="slider-container">
        <ApplicationBtn style="padding: 16px 0"></ApplicationBtn>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      slidersBlocks: [
        {
          title: 'Разработка сайтов',
          description:
            'Мы проводим глубокий анализ каждого проекта. Используем комплексный подход к проектированию прототипов и программной разработке, учитывающий особенности сферы деятельности вашего бизнеса.',
          swipersImg: [
            'make-site/one',
            'make-site/two',
            'make-site/three',
            'make-site/four',
            'make-site/five',
            'make-site/six',
          ],
        },
        {
          title: 'Редизайн сайтов',
          description:
            'Мы перерабатываем новое визуальное оформление вашего веб-сайта, навигацию и его содержимое для повышения его производительности и новых клиентов.',
          swipersImg: [
            'redisign/one',
            'redisign/two',
            'redisign/three',
            'redisign/four',
          ],
        },
        {
          title: 'Брэндинг',
          description:
            'Мы разрабатываем уникальную концепцию бренда вашей компании от логотипа до корпоративного стиля. Разрабатываем индивидуальный дизайн визиток, готовим материал к передачи в типографию. Разрабатываем дизайн упаковки товара.',
          swipersImg: [
            'brending/one',
            'brending/two',
            'brending/three',
            'brending/four',
            'brending/five',
          ],
        },
      ],
    }
  },
}
</script>

<style lang="scss">
  @media screen and (max-width: 960px) {
    .project__container {
      padding: 0;
    }
    .project__title {
      font-size: 28px;
      margin-bottom: 24px;
    }
    .project__desription {
      padding: 0;
      font-size: 16px;
    }
  }
</style>