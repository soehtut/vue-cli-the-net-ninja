<template>
  <h1>{{ title }}</h1>
  <!-- <Modal header="Sign Up" text="Create an account" /> -->
  <div v-if="showModal">
    <Modal :header="header" :text="text" theme="sale" @close="toggleModal" />
  </div>
  <p>Welcome....</p>
  <button @click="toggleModal">open modal</button>
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
      text: "Create an account",
      showModal: false
    }
  },
  methods: {
    handleClick() {
      console.log(this.$refs.name)
      this.$refs.name.classList.add('active')
      this.$refs.name.focus()
    },
    toggleModal() {
      this.showModal = !this.showModal
    }
  }
}
</script>

<style scoped>
h1 {
  color: red;
}
</style>
