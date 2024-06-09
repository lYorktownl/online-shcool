<template>
  <HeaderComponent />
  <SliderComponent @showModal="showModal"/>
  <ModalWindow :isVisible="isModalVisible" @close="closeModal" @submit="handleFormSubmit"/>
  <InfoBlock />
  <HelpAndSupport />
  <GalleryBlock />
  <MapApi />
  <FooterComponent />
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
import HeaderComponent from "./components/HeaderComponent.vue";
import SliderComponent from "./components/SliderComponent.vue";
import ModalWindow from "./components/ModalWindow.vue";
import InfoBlock from "./components/InfoBlock.vue";
import HelpAndSupport from "./components/HelpAndSupp.vue";
import GalleryBlock from "./components/GalleryBlock.vue";
import MapApi from "./components/MapApi.vue";
import FooterComponent from "./components/FooterComponent.vue";


export default defineComponent({
  name: "App",
  components: {
    HeaderComponent,
    SliderComponent,
    ModalWindow,
    InfoBlock,
    HelpAndSupport,
    GalleryBlock,
    MapApi,
    FooterComponent,
  },

  setup() {
    const isModalVisible = ref(false);

    const showModal = () => {
      isModalVisible.value = true;
    };

    const closeModal = () => {
      isModalVisible.value = false;
    };

    // eslint-disable-next-line @typescript-eslint/no-explicit-any
    const handleFormSubmit = (formData: any) => {
      console.log('Form submitted with data:', formData);
      // Handle form submission logic here
    };

    return {
      isModalVisible,
      showModal,
      closeModal,
      handleFormSubmit,
    };
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
@media (max-width: 320px) {
  #app {
    width: 320px;
  }
}
</style>
