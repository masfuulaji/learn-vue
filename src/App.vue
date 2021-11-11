<template>
  <h1>{{ title }}</h1>
  <div v-if="showModal">
    <Modal :header="header" :text="text" theme="book" @close="toggleModal"/>
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
      header: "Who Am I",
      text: "industrial society and its future",
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
