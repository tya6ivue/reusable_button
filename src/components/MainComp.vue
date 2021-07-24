<template>
  <div>
    <h1>{{ message }}</h1>
    <SecondaryComp @upDate="ForColor" />
    <br />
    <SecondaryComp @upDate="ForReverse" />
  </div>
</template>

<script>
import SecondaryComp from "./SecondaryComp.vue";
export default {
  name: "MainComp",
  components: {
    SecondaryComp,
  },

  data() {
    return {
      message: "Hello Vue.js!",
    };
  },
  methods: {
    ForColor() {
      alert("say hello");
    },
    ForReverse() {
      this.message = this.message.split("").reverse().join("");
    },
  },
};
</script>