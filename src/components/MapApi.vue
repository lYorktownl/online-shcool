<template>
  <div class="map-container">
    <div id="map" class="map"></div>
  </div>
</template>

<script lang="ts">
import { defineComponent, onMounted } from "vue";

declare global {
  interface Window {
    // eslint-disable-next-line @typescript-eslint/no-explicit-any
    ymaps: any;
  }
}

export default defineComponent({
  name: "YandexMap",
  setup() {
    const apiKey = "b5438323-2d34-4adb-bbfa-8967c30806ca";

    const loadYandexMapScript = (callback: () => void) => {
      const script = document.createElement("script");
      script.src = `https://api-maps.yandex.ru/2.1/?lang=ru_RU&apikey=${apiKey}`;
      script.onload = callback;
      document.head.appendChild(script);
    };

    onMounted(() => {
      loadYandexMapScript(() => {
        window.ymaps.ready(() => {
          const myMap = new window.ymaps.Map("map", {
            center: [55.028894, 82.926493], // Default center coordinates
            zoom: 15,
          });

          //  Adding a placemark
          const myPlacemark = new window.ymaps.Placemark(
            [55.028894, 82.926493],
            {
              balloonContent: "Moscow Center",
            }
          );

          myMap.geoObjects.add(myPlacemark);
        });
      });
    });

    return {};
  },
});
</script>

<style scoped>
.map-container {
  max-width: 1160px;
  height: 423px;
  margin: 60px auto 0 auto;
}

.map {
  width: 100%;
  height: 100%;
  border-radius: 30px;
}
@media (max-width: 320px) {
  .map-container {
    margin-top: 14px;
    width: 300px;
  }
}
</style>
