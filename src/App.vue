<template>
  <h1>{{ title }}</h1>
  <div v-if="showModal">
    <Modal theme="book" @close="toggleModal">
      <template v-slot:type>
        <span>Manifesto</span>
      </template>
      <h3>Who Am I</h3>
      <p>Industrial society and its future</p>
    </Modal>
  </div>
  <button @click="toggleModal">Just Click it</button>
</template>

<script>
import Modal from "./components/Modal.vue";

export default {
  name: "App",
  components: {
    Modal,
  },
  data() {
    return {
      title: "My App D:",
      showModal: false,
    };
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
