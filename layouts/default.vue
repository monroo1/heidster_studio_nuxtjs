<template>
   <div>
    <MobileNavComponent  v-if="width < 980" />
    <HeaderComponent v-else :class="headerClass"/>
    <Nuxt />
    <ScrollComponent v-if="windowTop > 700" />
    <LazyFooterComponent />
  </div>
</template>

<script>

export default ({
 data() {
    return {
      width: window.innerWidth,
      windowTop: window.scrollY,
      headerClass: '',
    };
  },
  mounted() {
    window.addEventListener("scroll", this.onScroll);
  },
  beforeUnmount() {
    window.removeEventListener("scroll", this.onScroll);
  },
  methods: {
    onScroll: function () {
      this.windowTop = window.top.scrollY;
      this.windowTop > 50 ? this.headerClass = 'headerScroll' : this.headerClass = '';
    },
    updateWidth() {
      this.width = window.innerWidth;
      
    },
    showDialog() {
      this.dialogVisible = true;
    },
    clickScroll() {
      window.scrollTo({
        top: 0,
        behavior: "smooth",
      });
    },
  },
  created() {
    window.addEventListener("resize", this.updateWidth);
  },
})
</script>
