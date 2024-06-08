<template>
  <HeaderComponent />
  <SliderComponent />
  <InfoBlock />
  <HelpAndSupport />
  <GalleryBlock />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import SliderComponent from "./components/SliderComponent.vue";
import HeaderComponent from "./components/HeaderComponent.vue";
import InfoBlock from "./components/InfoBlock.vue";
import HelpAndSupport from "./components/HelpAndSupp.vue";
import GalleryBlock from "./components/GalleryBlock.vue";

export default defineComponent({
  name: "App",
  components: {
    HeaderComponent,
    SliderComponent,
    InfoBlock,
    HelpAndSupport,
    GalleryBlock,
  },
});
</script>

<style lang="scss">
#app {
  width: 1400px;
  margin: 0 auto 0 auto;
  font-family: "Gilroy", sans-serif;
  color: #22253b;
}
</style>
