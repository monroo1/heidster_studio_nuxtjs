<template>
  <section class="arguments">
    <h2 class="arguments__title">
      {{ title }}
    </h2>
    <div class="argumnets__container wrapper">
      <div class="arguments__items">
        <article
          v-for="item in contents"
          :key="item.id"
          class="arguments__item"
        >
          <img :src="require(`~/assets/${item.icons}`)" class="arguments__item-img">
          <h3 class="arguments__item-title">
            {{ item.title }}
          </h3>
          <p class="arguments__item-description">
            {{ item.text }}
          </p>
        </article>
      </div>
      <img :src="require(`~/assets/img/arguments.svg`)" class="arguments__img">
    </div>
  </section>
</template>

<script>
export default {
  data () {
    return {
      title: 'Почему именно мы?',
      contents: [
        {
          id: 1,
          title: 'Конфиденциальность',
          icons: 'img/arguments-item.svg',
          text: 'Мы гарантируем сохранность вашей корпоративной информации от третьих лиц во время работы над проектом и после нее. Мы доверяем нашим клиентам, чтобы они доверяли нам.'
        },
        {
          id: 2,
          title: 'Ответственность',
          icons: 'img/arguments-item.svg',
          text: 'Мы понимаем важность каждого проекта. Наши сайты не только привлекательны внешне, но и удобны для пользователей и владельцев.'
        },
        {
          id: 3,
          title: 'Гибкость',
          icons: 'img/arguments-item.svg',
          text: 'Гибкая и поэтапная разработка, которая экономит ваше время и деньги.'
        }
      ]
    }
  }
}
</script>
