<template>
  <div>
    <h1>Home</h1>
    <HelloWorld v-bind:msg="`Welcome to your Vue.js App ${user}`" />
  </div>
</template>

<script>
import HelloWorld from "../components/HelloWorld";
import { mapState } from "vuex";

export default {
  name: "Home",
  data() {
    return {
      user: "Nathalie",
    };
  },
  computed: {
    count() {
      return store.state.user;
    },
  },
  components: {
    HelloWorld,
  },
};
</script>