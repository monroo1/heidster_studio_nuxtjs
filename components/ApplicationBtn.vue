<template>
  <div class="application">
    <div class="application__btn" @click="showDialog">Оставить заявку</div>
    <FormDialog v-if="showForm == true"/>
  </div>
</template>

<script>

export default({
  data () {
    return {
      showForm: false
    }
  },
  methods: {
    showDialog() {
      this.showForm = true
    },
    hideDialog() {
      this.showForm = false
    }
  }
})
</script>


<style>
.application {
  width: 100%;
  display: flex;
  justify-content: center;
}
.application__btn {
  text-decoration: none;
  cursor: pointer;
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
  color: #ff8833;
  border: 1px solid #ff8833;
  background-color: transparent;
  border-radius: 20px;
  padding: 20px 60px;
  font-weight: 600;
}
</style>
