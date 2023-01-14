<script lang="ts">
import type { PropType } from "vue";
import "./slotGameViewer.css";

type publisher = "yggdrasil" | "relax";

export default {
    props: {
        shouldShow: { type: Boolean, required: true },
        publisher: { type: String as PropType<publisher>, required: true },
        gameName: { type: String, required: true },
        gameId: { type: String, required: true },
        openOffsetX: { type: Number, required: true }
    },
    data() {
        return {
            currentOffsetX: 0
        }
    },
    emits: {
        onClose() { }
    },
    methods: {
        closeButtonClicked() {
            this.$emit("onClose");
        }
    },
    computed: {
        iframeSource() {
            if (this.publisher === "yggdrasil") {
                return "https://staticpff.yggdrasilgaming.com/init/launchClient.html?gameid=" + this.gameId + "&amp;lang=en&amp;currency=&amp;org=leovegas&amp;key=&amp;channel=pc&amp;skin=leovegas";
            } else {
                return "https://d1k6j4zyghhevb.cloudfront.net/casino/launcher.html?gameid=" + this.gameId + "&partner=leovegas&partnerid=13&channel=web&moneymode=fun&lang=en_US&apex=1&fullscreen=false";
            }
        }
    },
    mounted() {
        if (this.$refs.parent instanceof HTMLDivElement === false) {
            return;
        }

        const parent = this.$refs.parent as HTMLDivElement;

        const onWindowResize = () => {
            let width = window.visualViewport ? window.visualViewport.width : window.innerWidth;
            let height = window.visualViewport ? window.visualViewport.height : window.innerHeight;
            parent.style.width = width + "px";
            parent.style.height = height + "px";
        }

        window.addEventListener("resize", onWindowResize);
        onWindowResize();
    },
    watch: {
        openOffsetX(value) {
            this.currentOffsetX = value;

            const onRequestedAnimationFrame = () => {
                if (this.currentOffsetX < -1 || this.currentOffsetX > 1) {
                    requestAnimationFrame(onRequestedAnimationFrame);
                }
                this.currentOffsetX -= this.currentOffsetX * 0.1;
            }

            requestAnimationFrame(onRequestedAnimationFrame);
        }
    }
}
</script>

<template>
    <div :class="'slot_game_viewer' + (shouldShow ? '' : ' hidden')" ref="parent">
        <div class="background" @click="closeButtonClicked"></div>
        <h2>{{ gameName }}</h2>
        <div class="iframe_wrapper" :style="{ translate: `${currentOffsetX}px 0px` }">
            <p v-if="gameId !== '-1'">Loading...</p>
            <p v-if="gameId === '-1'">Game Unavailable</p>
            <iframe v-if="shouldShow" id="gameFrame" class="amG4g" :src="iframeSource" loading="eager" frameborder="0"
                scrolling="no" allow="autoplay"
                sandbox="allow-same-origin allow-scripts allow-forms allow-popups allow-popups-to-escape-sandbox allow-top-navigation allow-top-navigation-by-user-activation">
            </iframe>
        </div>
        <button class="close_button" @click="closeButtonClicked">X</button>
    </div>
</template>