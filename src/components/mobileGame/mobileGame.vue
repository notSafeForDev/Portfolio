<script lang="ts">
import "./mobileGame.css";
export default {
    props: {
        name: { type: String, required: true },
        videoUrl: { type: String, required: true },
        artStationUrl: { type: String, required: true }
    },
    mounted() {
        if (this.$refs.iframe instanceof HTMLIFrameElement === false) {
            return;
        }

        const iframe: HTMLIFrameElement = this.$refs.iframe as HTMLIFrameElement;

        new ResizeObserver((entries) => {
            iframe.style.height = (entries[0].contentRect.width * 2.1) + "px";
        }).observe(iframe);
    }
}
</script>

<template>
    <div class="mobile_game">
        <h3 class="centered">{{ name }}</h3>
        <div>
            <iframe ref="iframe" width="1120" height="630" :src="videoUrl" title="YouTube video player" frameborder="0"
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                allowfullscreen></iframe>
            <img src="@/assets/images/phone_overlay.png" />
        </div>
        <a :title="'more about ' + name" :href="artStationUrl" target="_blank" class="button centered">More</a>
    </div>
</template>