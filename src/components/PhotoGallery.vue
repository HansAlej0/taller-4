<template>
  <div class="photo-gallery">
    <photo-card v-for="photo in photos" :key="photo.id" :photo="photo"></photo-card>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import datos from "@/assets/json/datos.json";
import PhotoCard from "./PhotoCard.vue";

export default defineComponent({
  data() {
    return {
      photos: datos,
    };
  },
  components: {
    PhotoCard,
  },
});
</script>

<style scoped lang="scss">
.photo-gallery {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
}

</style>
