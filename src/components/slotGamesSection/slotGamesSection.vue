<script lang="ts">
import SlotGameViewer from '../slotGameViewer/slotGameViewer.vue';
import TechnologiesList from '../technologiesList/technologiesList.vue';
import Thumbnail from '../thumbnail/thumbnail.vue';

type publisher = "yggdrasil" | "relax";

type thumbnail = {
    title: string,
    publisher: publisher,
    id: string,
    hrefSuffix: string,
    imageUrlSuffix: string
}

export default {
    components: {
        Thumbnail,
        TechnologiesList,
        SlotGameViewer
    },
    data() {
        let thumbnails: thumbnail[] = [
            { title: "Jackpot Raiders", publisher: "yggdrasil", id: "7361", hrefSuffix: "jackpot-raiders", imageUrlSuffix: "X0LjA0151/ndD1rt8M1dbDBA-opt.jpg" },
            { title: "Aldo's Journey", publisher: "yggdrasil", id: "-1", hrefSuffix: "aldo-s-journey", imageUrlSuffix: "DlVZLmrwP/abblUr741Zjrr-opt.jpg" },
            { title: "Lucky Neko Gigablox", publisher: "yggdrasil", id: "10124", hrefSuffix: "lucky-neko-gigablox", imageUrlSuffix: "jJy5A9V7E/yBd3vUaKdAEQ7E.jpg" },
            { title: "Hades Gigablox", publisher: "yggdrasil", id: "10125", hrefSuffix: "hades-gigablox", imageUrlSuffix: "aeMR9gj3r/rleGulrxw0KDj.jpg" },
            { title: "Easter Island 2", publisher: "yggdrasil", id: "7396", hrefSuffix: "easter-island-2", imageUrlSuffix: "LGX1jxxql/dLJMfjQp44EPA.jpg" },
            { title: "Cluster Tumble", publisher: "relax", id: "clustertumble", hrefSuffix: "cluster-tumble", imageUrlSuffix: "VPP79vmxm/Q3xQCMMeDDrN8.jpg" },
            { title: "Beast Mode", publisher: "relax", id: "beastmode", hrefSuffix: "beast-mode", imageUrlSuffix: "1D9BoP3KN/3vO7Hx7dkJWPD.jpg" },
            { title: "Temple Tumble 2 Dream Drop", publisher: "relax", id: "templetumble2dd", hrefSuffix: "temple-tumble-2-dream-drop", imageUrlSuffix: "MqXY5yA4v/BpB4txMdpxnKX.jpg" },
            { title: "Dead Riders Trail", publisher: "relax", id: "deadriderstrail", hrefSuffix: "dead-riders-trail", imageUrlSuffix: "bvnQwl93X/Ll0QHldvJrYEN.jpg" },
            { title: "Net Gains", publisher: "relax", id: "netgains", hrefSuffix: "net-gains", imageUrlSuffix: "aeXNXxrML/5WaQSkMaMWkOA.jpg" }
        ];

        return {
            countLimit: Infinity,
            isExpanded: false,
            thumbnails,
            shouldShowGame: false,
            gameName: "",
            publisher: "yggdrasil" as publisher,
            gameId: ""
        }
    },
    methods: {
        onResize() {
            this.countLimit = (window.innerWidth <= 460 && this.isExpanded === false) ? 4 : Infinity;
        },
        onThumbnailClick(thumbnail: thumbnail) {
            this.shouldShowGame = true;
            this.gameName = thumbnail.title;
            this.publisher = thumbnail.publisher;
            this.gameId = thumbnail.id;
        },
        onSlotGameViewerClose() {
            this.shouldShowGame = false;
            this.gameName = "";
            this.gameId = "";
        },
        onShowMoreGamesButtonClick() {
            this.isExpanded = true;
            this.countLimit = Infinity;
        }
    },
    mounted() {
        window.addEventListener("resize", this.onResize);
        this.onResize();
    }
}
</script>

<template>
    <div>
        <div class="dark_gray full_width slanted slanted_5 overlap_down_200px highlight_bottom">
            <div class="spacer_large"></div>
        </div>
        <h2>Online Casino Games</h2>
        <h3>2019 - 2023</h3>
        <div class="grid">
            <Thumbnail v-for="thumbnail in thumbnails.slice(0, countLimit)" :title="thumbnail.title"
                :image-src="'https://ik.imagekit.io/leovegas/lv/games/' + thumbnail.imageUrlSuffix"
                @click="onThumbnailClick(thumbnail)" />
            <button v-if="countLimit < Infinity && !isExpanded" class="text_button"
                @click="onShowMoreGamesButtonClick">{{ "And " + (thumbnails.length - countLimit) + " More..." }}
            </button>
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
        <TechnologiesList :items="[
            { name: 'PixiJS', description: 'WebGL rendering framework', link: 'https://pixijs.com/' },
            { name: 'React', description: 'Used for rendering PixiJS elements and UI', link: 'https://reactjs.org/' },
            { name: 'Redux', description: 'State management', link: 'https://redux.js.org/' },
            { name: 'Redux-Saga', description: 'Used to create the asynchronous game flows', link: 'https://redux-saga.js.org/' }
        ]" />
        <SlotGameViewer :should-show="shouldShowGame" :game-name="gameName" :publisher="publisher" :game-id="gameId"
            @onClose="onSlotGameViewerClose" />
    </div>
</template>