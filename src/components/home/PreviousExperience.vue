<template>
  <div class="mt-5">
    <title-header :title="'Join the Kusama Ecosystem'" />
    <ul
      class="row col-lg-9 col-md-10 pt-4 col-sm-12 mx-auto d-flex justify-center"
    >
      <li class="col-2" v-for="(company, index) in ecoSystem" :key="index">
        <img :src="company.image" alt="" />
        <div class="text" v-text="company.name" />
      </li>
    </ul>
  </div>
</template>

<script>
import { ref } from "vue";
import TitleHeader from "./TitleHeader";
import polkadot from "@/assets/polkadot.png";
import acala from "@/assets/acala.png";
import chainlink from "@/assets/chainlink.png";
import moonbeam from "@/assets/moonbeam.png";
import phala from "@/assets/phala.svg";
import edgeware from "@/assets/edgeware.svg";
export default {
  components: {
    TitleHeader,
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
      {
        name: "Moonbeam",
        image: moonbeam,
      },
      {
        name: "Phala",
        image: phala,
      },
      {
        name: "Edgeware",
        image: edgeware,
      },
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
      {
        name: "Moonbeam",
        image: moonbeam,
      },
      {
        name: "Phala",
        image: phala,
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
@import "../../scss/shared/mixins.scss";
li {
  list-style-type: none;
  img {
    width: 42px;
    height: 42px;
    border-radius: 50%;
  }
  .text {
    color: $lighter-white;
    font-size: 14px;
    @include space-mono-font();
  }
}
</style>
