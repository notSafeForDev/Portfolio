<script lang="ts">
import "./imageLink.css";
export default {
    props: {
        title: { type: String, required: true },
        href: { type: String, required: true },
        src: { type: String, required: true }
    }
}
</script>

<template>
    <a class="image_link" :title="title" :href="href" target="_blank">
        <div>
            <img :src="src" />
        </div>
    </a>
</template>