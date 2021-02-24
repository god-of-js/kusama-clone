<template>
  <div class="testimonial m-3 p-3" id="reccomendator">
    <div class="img_cont pb-4">
      <img :src="avatar" alt="" />
    </div>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Nisi id minima
      accusamus expedita esse dignissimos eum cum eligendi quaerat suscipit
      nobis, quibusdam aperiam obcaecati fugit distinctio porro, ipsa ut ad?
    </p>
    <hr class="mt-5">
    <div class="text-center name" v-text="name" />
  </div>
</template>

<script>
export default {
  props: {
    avatar: {
      type: File,
    },
    name: {
      type: String,
      default: "",
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../../scss/colors.scss";
@import "../../scss/shared/mixins.scss";
.testimonial {
  color: $white;
  background-color: $background-color-black;
  width: 100%;
  border: 1px solid $white;
  border-radius: 5px;
  height: 400px;
  @include  space-mono-font();
  .name {

  }
}
img {
  border-radius: 50%;
}
p {
  font-size: 0.9em;
}
hr {
  width: 30%;
  background-color: $white;
}
</style>