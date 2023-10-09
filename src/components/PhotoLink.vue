<template>
    <div class="photo-link">
        <a :href="link" target="_blank">Ver mas sobre el pais</a>
    </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
    props: {
        link: String,
    },
});
</script>

<style scoped lang="scss">
.photo-link a {
    display: flex;
    justify-content: center;
    padding: 5px;
    margin: 5px;
    text-decoration: none;
    color: white;
    background-color: #007bff;
    border: 1px solid #ccc;
    border-radius: 5px;

    &:hover{
        text-decoration: none;
    }
}
</style>
