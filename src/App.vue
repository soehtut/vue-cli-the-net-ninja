<template>
  <h1>{{ title }}</h1>
  <!-- <Modal header="Sign Up" text="Create an account" /> -->
  <div v-if="showModal">
    <Modal theme="sale" @close="toggleModal">
      <h1>Sign Up</h1>
      <p>Create an account</p>
      <template v-slot:links>
        <a href="#">sign up now</a>
        <a href="#">more info</a>
      </template>
    </Modal>
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

<style>
h1 {
  color: red;
}
</style>
