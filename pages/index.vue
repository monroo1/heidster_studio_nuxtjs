<template>
  <main>
    <IntroductionComponent />
    <BenefitsComponent />
    <ArgumentsComponent />
    <ClientsComponent />
  </main>
</template>

<script>
export default {
  data() {
      return {
        title: 'Heidster Studio'
      }
    },
    head() {
      return {
        title: this.title, 
      }
    }
}
</script>
