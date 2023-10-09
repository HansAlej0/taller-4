<template>
    <div class="photo-image">
        <img :src="require(`@/assets/img/${photo.image}`)" :alt="photo.title" />
    </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
    props: {
        photo: {
            type: Object,
            default: "",
        },
    },
});
</script>

<style scoped lang="scss">
.photo-image img {
    max-width: 100%;
    height: auto;
    border-radius: 5px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease-in-out;

    &:hover{
        transform: scale(1.05);
    }
}
</style>
