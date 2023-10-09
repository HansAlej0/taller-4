<template>
  <photo-gallery />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import PhotoGallery from "./components/PhotoGallery.vue";

export default defineComponent({
  components: {
    PhotoGallery,
  },
});
</script>
