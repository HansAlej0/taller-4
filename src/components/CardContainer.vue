<template>
    <div class="card-container">
        <Card v-for="post in posts" :key="post.title" :title="post.title" :text="post.text" :link="post.link"/>
    </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import datos from "@/assets/json/datos.json";
import Card from "./Card.vue";

export default defineComponent({
    name: "CardContainer",
    components: {
        Card
    },
    computed: {
        posts: () => {
            return datos.map((post: any) => {
                return post;
            });
        },
    },
});
</script>

<style scoped lang="scss">
</style>