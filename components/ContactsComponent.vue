<template>
  <div>
    <section class="contacts">
      <h2 class="contacts__title">
        {{ title }}
      </h2>
      <p class="contacts__title-description">
        {{ subtitle }}
      </p>
      <div class="contacts__container wrapper">
        <ul class="contacts__list">
          <li v-for="li in ulContacts" :key="li.id" class="contacts__list-item">
            {{ li.content }}
          </li>
        </ul>

        <form class="contacts__form">
          <input
            class="contacts__form-input"
            type="email"
            placeholder="Ваш E-mail"
          >
          <input
            class="contacts__form-input"
            type="text"
            placeholder="Ваше имя"
          >
          <textarea
            class="contacts__form-input"
            placeholder="Текст отзыва"
            rows="450"
          />
          <button class="contacts__form-btn">
            Отправить
          </button>
        </form>
      </div>
    </section>
    <section class="contacts-map">
      <GMap
        ref="gMap"
        language="en"
        :cluster="{options: {styles: clusterStyle}}"
        :center="{lat: locations[0].lat, lng: locations[0].lng}"
        :options="{fullscreenControl: false }"
        :zoom="15"
      >
      <!-- styles: mapStyle -->
        <GMapMarker
          v-for="location in locations"
          :key="location.id"
          :position="{lat: location.lat, lng: location.lng}"
          @click="currentLocation = location"
        >
          <GMapInfoWindow :options="{maxWidth: 200}">
            <code>
              lat: {{ location.lat }},
              lng: {{ location.lng }}
            </code>
          </GMapInfoWindow>
        </GMapMarker>
        <!-- <GMapCircle :options="circleOptions"/> -->
      </GMap>
    </section>
  </div>
</template>

<script>
export default {
  data () {
    return {
      title: 'Контакты',
      subtitle:
        'Свяжитесь с нами любым удобным способом для вас, мы будем рады сотрудничеству',
      ulContacts: [
        { id: 1, content: '+7 (951) 535 38 39' },
        { id: 2, content: '+7 (950) 858 25 11' },
        { id: 3, content: 'heidster.studio@gmail.com' },
        {
          id: 4,
          content:
            'г. Ростов-на-Дону, ул. Металлургическая 102/2, 4 этаж, офис 406'
        }
      ],
      currentLocation: {},
    // circleOptions: {
    //   ...
    // },
      locations: [
        {
          lat: 47.254895,
          lng: 39.771068
        },
      ],
      // mapStyle: [...],
      clusterStyle: [
        {
          url: "https://developers.google.com/maps/documentation/javascript/examples/markerclusterer/m1.png",
          width: 56,
          height: 56,
          textColor: "#fff"
        }
      ]
    }
  }
}
</script>
