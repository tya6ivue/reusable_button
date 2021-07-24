<template>
  <div>
    <button @click="upDateeee">Add data</button>

    <h1>{{ data.name }} {{ data.lastName }}</h1>
  </div>
</template>

<script>
export default {
  name: "SecondaryComp",
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