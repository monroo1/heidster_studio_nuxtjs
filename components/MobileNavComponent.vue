<!--yes -->
<template>
  <section class="mobile-nav">
    <div class="mobile-nav__container">
      <div v-for="link in links" :key="link.id" class="mobile-nav__item">
        <router-link :to="link.route" class="mobile-nav__link">
          <div class="mobile-nav__link-logo">
            <img :src="link.src" alt="img" class="mobile-nav__link-img">
          </div>
          <div class="mobile-nav__link-text">
            {{ link.text }}
          </div>
        </router-link>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data () {
    return {
      links: [
        { id: 1, text: 'Компания', route: '/', src: 'img/icons/home.svg' },
        {
          id: 2,
          text: 'Услуги',
          route: '/services',
          src: 'img/icons/services.svg'
        },
        {
          id: 3,
          text: 'Проекты',
          route: '/projects',
          src: 'img/icons/projects.svg'
        },
        {
          id: 4,
          text: 'Контакты',
          route: '/contacts',
          src: 'img/icons/contacts.svg'
        }
      ]
    }
  }
}
</script>
