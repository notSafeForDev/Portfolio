<script lang="ts">
import "./thumbnail.css";
export default {
    props: {
        title: String,
        href: String,
        imageSrc: String
    }
}
</script>

<template>
    <a :title="title + ' thumbnail'" class="thumbnail" :href="href" target="_blank">
        <img :src="imageSrc" />
        <span>{{ title }}</span>
    </a>
</template>