<template>
  <div class="sroll-up" @click="clickScroll">
    <img src="~/assets/img/icons/scroll.png"> 
  </div>
</template>

<script>
export default {
   methods: {
    clickScroll() {
      this.$parent.clickScroll()
    },
  },
}
</script>