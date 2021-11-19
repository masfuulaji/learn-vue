<template>
  <div class="home">Home</div>
  <p ref="p">My name is {{ name }} and my age is {{ age }}</p>
  <button @click="clickThis">Just Click It</button>
  <input type="text" v-model="name" />
</template>

<script>
import { ref } from "@vue/reactivity";
// @ is an alias to /src

export default {
  name: "Home",
  setup() {
    const name = ref("budi");
    const age = ref(20);

    // const p = ref(null);

    const clickThis = () => {
      name.value = "dimas";
      age.value = "30";
    };

    return { name, age, clickThis };
  },
};
</script>
