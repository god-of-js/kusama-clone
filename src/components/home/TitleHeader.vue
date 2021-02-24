<template>
  <div v-text="title"  class="heading" />
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: ""
    }
  }
};
</script>

<style lang="scss" scoped>
@import "../../scss/colors.scss";
div {
  font-size: 35px;
  color: $white;
  width: 100%;
  font-weight: bold;
}
</style>
