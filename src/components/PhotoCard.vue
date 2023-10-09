<template>
    <div class="photo-card">
        <photo-image :photo="photo"></photo-image>
        <div class="photo-info">
            <h2>{{ photo.title }}</h2>
            <photo-link :link="photo.link"></photo-link>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import PhotoImage from "./PhotoImage.vue";
import PhotoLink from "./PhotoLink.vue";

export default defineComponent({
    props: {
        photo: {
            type: Object,
            default: "",
        },
    },
    components: {
        PhotoImage,
        PhotoLink,
    },
});
</script>

<style scoped lang="scss">
.photo-card {
    width: 250px;
    margin: 15px;
    padding: 10px;
    border: 2px solid #ccc;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    border-radius: 5px;
    background-color: #f5f5f5;
    color: #333;
    transition: transform 0.3s ease-in-out;

    h2 {
        font-size: 18px;
        text-align: center;
    }

    &:hover {
        transform: scale(1.05);
    }
}

.photo-link{
    font-size: 14px;
}

.photo-info {
    margin-top: 20px;
}
</style>
