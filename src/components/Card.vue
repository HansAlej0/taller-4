<template>
    <div class="card">
        <h3>{{ title }}</h3>
        <p>{{ text }}</p>
        <a :href="link" target="_blank">Enlace</a>
    </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import datos from "@/assets/json/datos.json";

export default defineComponent({
    name: "Card",
    props: {
        title: {
            type: String,
            default: "",
        },
        text: {
            type: String,
            default: "",
        },
        link: {
            type: String,
            default: "",
        },
    },
});
</script>

<style scoped lang="scss">
.card{
    border: 1px solid #ccc;
    padding: 16px;
    margin: 16px;
    display: flex;
    flex-direction: column;
    align-items: center;
    max-width: 300px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    background-color: #fff;
}
</style>
