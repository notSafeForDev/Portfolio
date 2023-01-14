<script lang="ts">
import "./thumbnail.css";
export default {
    props: {
        title: { type: String, required: true },
        href: { type: String, required: false },
        imageSrc: { type: String, required: true }
    }
}
</script>

<template>
    <a :title="title.toLowerCase() + ' thumbnail'" class="thumbnail" :href="href" target="_blank">
        <img :src="imageSrc" />
        <span>{{ title }}</span>
    </a>
</template>