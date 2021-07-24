<template>
  <div>
    <ul>
      <li v-for="(value, index) in values" :key="index">
        {{ value.brands }} {{ value.types }}
      </li>
    </ul>

    <SecondaryComp :data="users" @upDate="upDate" />
    <SecondaryComp :data="users" @upDate="upDate" />
  </div>
</template>

<script>
import SecondaryComp from "./SecondaryComp.vue";
export default {
  name: "ParenComp",
  components: {
    SecondaryComp,
  },

  data() {
    return {
      users: { name: "nishant", lastName: "tyagi" },
      values: [],
    };
  },
  methods: {
    upDate() {
      this.values.push({
        brands: "coco-cola",
      });
    },
  },
};
</script>