<template>
  <div>
    <img
      :id="id"
      class="img"
      :src="require(`@/assets/${image}.png`)"
      :alt="desc"
    />
  </div>
</template>
<script>
export default {
  name: "ImageBase",
  props: {
    image: String,
    desc: String,
    id: String,
  }
};
</script>

<style lang="sass" scoped>
  @import'./ImageBase.scss'
</style>
