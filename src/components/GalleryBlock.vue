<template>
  <div class="main">
    <div class="gallery-grid">
      <a
        :href="require('@/assets/photos/gallery/twoWomen.png')"
        data-fancybox="gallery"
        class="large"
      >
        <img
          :src="require('@/assets/photos/gallery/twoWomen.png')"
          alt="twoWomen"
        />
      </a>
      <a
        :href="require('@/assets/photos/gallery/keyboard.png')"
        data-fancybox="gallery"
      >
        <img
          :src="require('@/assets/photos/gallery/keyboard.png')"
          alt="keyboard"
        />
      </a>
      <a
        :href="require('@/assets/photos/gallery/notebookHandclock.png')"
        data-fancybox="gallery"
      >
        <img
          :src="require('@/assets/photos/gallery/notebookHandclock.png')"
          alt="notebookHandclock"
        />
      </a>
      <a
        :href="require('@/assets/photos/gallery/notebookYellowShirt.png')"
        data-fancybox="gallery"
      >
        <img
          :src="require('@/assets/photos/gallery/notebookYellowShirt.png')"
          alt="notebookYellowShirt"
        />
      </a>
      <a
        :href="require('@/assets/photos/gallery/kid.png')"
        data-fancybox="gallery"
      >
        <img :src="require('@/assets/photos/gallery/kid.png')" alt="kid" />
      </a>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import { Fancybox } from "@fancyapps/ui";
import "@fancyapps/ui/dist/fancybox/fancybox.css";

export default defineComponent({
  mounted() {
    Fancybox.bind('[data-fancybox="gallery"]', {
      // Custom options can be set here
    });
  },
});
</script>

<style scoped>
.main {
  margin: 0 auto 0 auto;
  max-width: 1160px;
}
.gallery-grid {
  display: grid;
  grid-template-columns: 571px 275px 275px;
  grid-template-rows: 275px 275px;
  gap: 20px;
}

.gallery-grid a.large {
  grid-row: span 2;
  height: 571px;
}

.gallery-grid a {
  display: block;
  width: 100%;
  height: 100%;
}

.gallery-grid img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
@media (max-width: 870px) {
  .gallery-grid {
    grid-template-columns: 1fr 1fr;
  }

  .gallery-grid a.large {
    grid-column: span 1;
    height: auto;
  }
}
@media (max-width: 320px) {
  .main {
    width: 300px;
    padding: 10px;
  }

  .gallery-grid {
    display: grid;
    grid-template-columns: 1fr 1fr; /* Two columns */
    grid-template-rows: auto; /* Automatically sized rows */
    gap: 10px;
  }

  .gallery-grid a.large {
    grid-column: span 2;
    width: 300px;
    height: 300px; /* Span two columns */
  }

  .gallery-grid a {
    width: 145px;
    height: auto;
  }

  .gallery-grid img {
    width: 100%;
    height: auto;
  }
}
</style>
