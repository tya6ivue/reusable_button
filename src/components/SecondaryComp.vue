<template>
  <div>
    <button class="button" @click="upDateeee">Primary</button>
  </div>
</template>

<script>
export default {
  name: "ChildComp",
  props: {
    data: {
      type: Object,

      default: () => ({}),
    },
  },
  methods: {
    upDateeee() {
      this.$emit("upDate");
    },
  },
};
</script>

<style scoped>
.button {
  background-color: #0069d9;
  color: #ffff;
  border-radius: 5px;
  width: 100px;
}
</style>