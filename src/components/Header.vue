<template>
  <h2>Hello World</h2>
  <br />
  <h2>{{ text }}</h2>
  <button @click="changeText">Ubah Text</button>
</template>

<script>
export default {
  name: "Header",
  props: ["text"],
  data() {
    return {
      newText: "Ini adalah text dari header.vue",
    };
  },
  methods: {
    changeText() {
      this.$emit("changeTitle", this.newText);
    },
  },
  emits: ["changeTitle"],
};
</script>

<style></style>
