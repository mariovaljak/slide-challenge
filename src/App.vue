<template>
  <div class="page">
    <global-header />
    <global-footer />
    <block-work
      v-for="person in people"
      :image="person.image"
      :name="person.name"
      :workName="person.workName"
      :key="person.name"
    />
  </div>
</template>

<script>
import GlobalHeader from "./components/GlobalHeader.vue";
import GlobalFooter from "./components/GlobalFooter.vue";
import BlockWork from "./components/BlockWork.vue";

let people = [
  {
    name: "Lorin Askill",
    workName: "Sia - The Greatest",
    image: "sia-header-1.png",
  },
  {
    name: "Conor O’Neill",
    workName: "Toyota — Highlander Heroes",
    image: "./assets/Toyota - Highlanders Heroes.png",
  },
  {
    name: "Stephania Dulowski",
    workName: "Rainn — Wait",
    image: "./assets/WaitPSA_60_Bold.png",
  },
  {
    name: "Shane Reid",
    workName: "Adidas Originals — Original Is Never Finished",
    image: "./assets/Website.png",
  },
  {
    name: "Grant Surmi",
    workName: "Zelle — Pay It Safe",
    image: "./assets/ZELLE_0.png",
  },
  {
    name: "Kyle Brown",
    workName: "GE — Enhance Your Lighting",
    image: "./assets/GE_0.png",
  },
];

export default {
  data() {
    return {
      people,
    };
  },
  name: "App",
  components: { GlobalHeader, GlobalFooter, BlockWork },
};
</script>

<style>
body {
  color: white;
}
</style>
