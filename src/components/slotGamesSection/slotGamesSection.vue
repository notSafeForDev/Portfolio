<script lang="ts">
import Thumbnail from '../thumbnail/thumbnail.vue';

export default {
    components: {
        Thumbnail
    },
    data() {
        return {
            countLimit: Infinity,
            thumbnails: [
                { title: "jackpot raiders", hrefSuffix: "jackpot-raiders", imageUrlSuffix: "X0LjA0151/ndD1rt8M1dbDBA-opt.jpg" },
                { title: "aldo's journey", hrefSuffix: "aldo-s-journey", imageUrlSuffix: "DlVZLmrwP/abblUr741Zjrr-opt.jpg" },
                { title: "lucky neko gigablox", hrefSuffix: "lucky-neko-gigablox", imageUrlSuffix: "jJy5A9V7E/yBd3vUaKdAEQ7E.jpg" },
                { title: "hades gigablox", hrefSuffix: "hades-gigablox", imageUrlSuffix: "aeMR9gj3r/rleGulrxw0KDj.jpg" },
                { title: "easter island 2", hrefSuffix: "easter-island-2", imageUrlSuffix: "LGX1jxxql/dLJMfjQp44EPA.jpg" },
                { title: "cluster tumble", hrefSuffix: "cluster-tumble", imageUrlSuffix: "VPP79vmxm/Q3xQCMMeDDrN8.jpg" },
                { title: "beast mode", hrefSuffix: "beast-mode", imageUrlSuffix: "1D9BoP3KN/3vO7Hx7dkJWPD.jpg" },
                { title: "temple tumble 2 dream drop", hrefSuffix: "temple-tumble-2-dream-drop", imageUrlSuffix: "MqXY5yA4v/BpB4txMdpxnKX.jpg" },
                { title: "dead riders trail", hrefSuffix: "dead-riders-trail", imageUrlSuffix: "bvnQwl93X/Ll0QHldvJrYEN.jpg" },
                { title: "net gains", hrefSuffix: "net-gains", imageUrlSuffix: "aeXNXxrML/5WaQSkMaMWkOA.jpg" }
            ]
        }
    },
    methods: {
        onResize() {
            this.countLimit = window.innerWidth <= 770 ? 4 : Infinity;
        },
    },
    mounted() {
        window.addEventListener("resize", this.onResize);
        this.onResize();
    }
}
</script>

<template>
    <div>
        <div class="black full_width slanted_5 overlap_down_200px highlight_bottom">
            <div class="spacer_large"></div>
        </div>
        <h2>Online Slot Games</h2>
        <h3>2019 - 2023</h3>
        <div class="grid">
            <Thumbnail v-for="thumbnail in thumbnails.slice(0, countLimit)" :title="thumbnail.title"
                :href="'https://www.leovegas.com/en-row/game/' + thumbnail.hrefSuffix"
                :image-src="'https://ik.imagekit.io/leovegas/lv/games/' + thumbnail.imageUrlSuffix" />
            <p v-if="countLimit < Infinity" class="centered">{{
                "And " + (thumbnails.length - countLimit) + " More..."
            }}</p>
        </div>
        <p>I started working for Yggdrasil Gaming, creating online casino games in 2019. I got called the "Particle
            Man" at one point, due to my "expertize" with particle effects. Among particles, I worked on a lot of the
            effects and timings to make the game as satisfying to play as possible.</p>
        <p>In 2021, our studio got acquired by Relax Gaming LTD, where our team continued working as a close and well
            oiled machine. We got tasked with building some of the Relax's highest profile games, including a sequel to
            the highly popular game:
            <a href="https://www.leovegas.com/en-row/game/temple-tumble-megaways" target="_blank">Temple Tumble
                MEGAWAYS</a>.
        </p>
        <div class="spacer_small"></div>
        <h3>Technologies</h3>
        <ul>
            <li><a href="https://pixijs.com/">PixiJS</a>WebGL rendering framework</li>
            <li><a href="https://reactjs.org/">React</a>Rendering framework</li>
            <li><a href="https://redux.js.org/">Redux</a>State management</li>
            <li><a href="https://redux-saga.js.org/">Redux-Saga</a>Used to create asynchronous application flows</li>
        </ul>
    </div>
</template>