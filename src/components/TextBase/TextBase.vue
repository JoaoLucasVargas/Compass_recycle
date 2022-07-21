<template>
  <p :class="size" :id="id" :text="text">{{ text }}</p>
</template>

<script>
export default {
  name: "TextBase",
  props: {
    size: {
      type: String,
    },
    text: {
      type: String,
    },
    id: {
      type: String,
    },
  },
};
</script>

<style lang="scss" scoped>
@import "./TextBase.scss";
</style>
