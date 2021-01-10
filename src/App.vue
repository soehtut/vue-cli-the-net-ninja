<template>
  <h1>{{ title }}</h1>
  <!-- <Modal header="Sign Up" text="Create an account" /> -->
  <Modal :header="header" :text="text" theme="sale" />
</template>

<script>
import Modal from './components/Modal'

export default {
  name: 'App',
  components: {
    Modal
  },
  data() {
    return {
      title: 'My First Vue App :)',
      header: "Sign Up",
      text: "Create an account"
    }
  },
  methods: {
    handleClick() {
      console.log(this.$refs.name)
      this.$refs.name.classList.add('active')
      this.$refs.name.focus()
    }
  }
}
</script>

<style scoped>
h1 {
  color: red;
}
</style>
