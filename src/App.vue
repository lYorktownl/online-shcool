<template>
  <HeaderComponent />
  <SliderComponent />
  <InfoBlock />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import SliderComponent from "./components/SliderComponent.vue";
import HeaderComponent from "./components/HeaderComponent.vue";
import InfoBlock from "./components/InfoBlock.vue";

export default defineComponent({
  name: "App",
  components: {
    HeaderComponent,
    SliderComponent,
    InfoBlock,
  },
});
</script>

<style lang="scss">
#app {
  width: 1400px;
  margin: 0 auto 0 auto;
  font-family: 'Gilroy', sans-serif;
  color: #22253b;
}
</style>
