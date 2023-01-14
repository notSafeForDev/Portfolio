<script lang="ts">
import Sticker from '../sticker/sticker.vue';
import TechnologiesList from '../technologiesList/technologiesList.vue';
import VideoPlayer from '../videoPlayer/videoPlayer.vue';

export default {
    components: { TechnologiesList, VideoPlayer, Sticker }
}
</script>

<template>
    <div>
        <div class="black full_width slanted_5 overlap_down_200px highlight_bottom">
            <div class="spacer_large"></div>
        </div>
        <h2>Video Player</h2>
        <h3>2022</h3>
        <VideoPlayer>
            <Sticker text="18+ Adult Only" />
        </VideoPlayer>
        <p>It started on Reddit of all places. I got tasked by a VR production company to create their web based
            video player for their sites. Having dabbled with VR in Unity prior to that, I realized that I was prepared
            for the task at hand.</p>
        <p>After quickly realizing that Unity didn't load quite fast enough on the web, I ended up learning Babylon.js,
            and the rest is history.</p>
        <p>The player can be found live at <a title="fuckpassvr website" href="https://www.fuckpassvr.com/" target="_blank">fuckpassvr.com</a>.</p>
        <p>It even supports <a href="https://www.thehandy.com/" target="_blank">theHandy</a>, an interactive sex toy that syncs with the video content.</p>
        <TechnologiesList :items="[
            { name: 'Babylon.js', description: '3D & XR rendering engine', link: 'https://www.babylonjs.com/' },
            { name: 'Typescript', description: 'Superset of Javascript', link: 'https://www.typescriptlang.org/' },
            { name: 'Web component', description: 'For making the player embeddable', link: 'https://www.webcomponents.org/introduction' }
        ]" />
    </div>
</template>