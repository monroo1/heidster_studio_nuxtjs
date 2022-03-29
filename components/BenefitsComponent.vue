
<template>
  <section class="benefits wrapper">
    <div class="benefits-title">
      <h2 class="benefits-title__title">
        {{ title }}
      </h2>
      <span class="benefits-title__description">{{ subtitle }}</span>
    </div>
    <div class="benefits-content">
      <article v-for="item in contents" :key="item.id" class="benefits-block">
        <h3 class="benefits-block__title">
          {{ item.title }}
        </h3>
        <p class="benefits-block__description">
          {{ item.text }}
        </p>
        <span class="benefits-block__number">{{ item.icons }}</span>
      </article>
    </div>
  </section>
</template>

<script>
export default {
  data () {
    return {
      title: 'Наши преимущества',
      subtitle: 'Без бюрократии, задержек при обработке заявок',
      contents: [
        {
          id: 1,
          title: 'Качество',
          icons: '01',
          text: 'Ведение поэтапной разработки проекта - залог стабильной работы сайта. Качество достигается путем тщательного контроля на всех этапах работы, вплоть до запуска проекта.'
        },
        {
          id: 2,
          title: 'Креативность  ',
          icons: '02',
          text: 'Мы ориентируемся на чистый, аккуратный и минималистичный дизайн. Создаем продуманные сайты, используя готовые и уникальные решения.'
        },
        {
          id: 3,
          title: 'Индивидуальный подход',
          icons: '03',
          text: 'Наша компания работает по принципу индивидуального подхода к каждому клиенту. Этот метод позволяет нам добиваться успеха в решении задач всех уровней.'
        }
      ]
    }
  }
}
</script>
