<template>
  <div class="testimonials pt-4">
    <div class="testimonials-tag mb-4">Testimonials</div>
    <title-header :title="'Participants say'" />
    <div class="row pt-4" id="reccomendators">
      <div
        class="col-lg-4 col-sm-10 mx-auto col-md-4"
        v-for="(client, index) in ecoSystem"
        :key="index"
      >
        <testimonial :avatar="client.image" :name="client.name" />
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
import titleHeader from "./TitleHeader";
import Testimonial from "./Testimonial";
import polkadot from "@/assets/polkadot.png";
import acala from "@/assets/acala.png";
import chainlink from "@/assets/chainlink.png";
export default {
  components: {
    titleHeader,
    Testimonial,
  },
  setup() {
    const ecoSystem = ref([
      {
        name: "Polkadot",
        image: polkadot,
      },
      {
        name: "Acala",
        image: acala,
      },
      {
        name: "Chainlink",
        image: chainlink,
      },
    ]);
    return {
      ecoSystem,
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../scss/colors.scss";
::v-deep {
  .heading {
    font-size: 25px;
    text-align: left;
  }
}
.testimonials-tag {
  width: fit-content;
  background: $pink;
  color: $lighter-white;
  padding: 5px 8px;
  font-size: 0.7em;
  border-radius: 15px;
}
</style>