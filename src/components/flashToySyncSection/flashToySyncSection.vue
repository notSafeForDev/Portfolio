<script lang="ts">
import ImageLink from '../imageLink/imageLink.vue';
import Sticker from '../sticker/sticker.vue';
import TechnologiesList from '../technologiesList/technologiesList.vue';

export default {
    components: { ImageLink, Sticker, TechnologiesList }
}
</script>

<template>
    <div>
        <div class="black full_width slanted_5 overlap_down_200px highlight_bottom">
            <div class="spacer_large"></div>
        </div>
        <h2>Flash Toy Sync</h2>
        <h3>2020 / 2022</h3>
        <ImageLink title="flash toy sync" href="https://imgur.com/a/lkGZJ4z" src="https://i.imgur.com/loT4QVr.png">
            <Sticker text="18+ Adult Only" />
        </ImageLink>
        <p class="inline_block">My journey with <a href="https://www.thehandy.com/" target="_blank">theHandy</a> started
            here.</p>
        <p>
            An application that I built to allow almost any Flash animation found on the net to control theHandy. Built
            to breath
            new life into content that was created in the past decades. And as an homage to the technology that got me
            into
            development, back in 2005.
        </p>
        <a href="https://github.com/notSafeForDev/flash-toy-sync-v3" target="_blank">Github
            (https://github.com/notSafeForDev/flash-toy-sync-v3)</a>
        <div class="spacer_small"></div>
        <TechnologiesList :items="[
            { name: 'Flash', description: 'Multimedia software platform', link: 'https://get.adobe.com/flashplayer/about' },
            { name: 'ActionScript 3.0', description: 'Primary programing language', link: 'https://en.wikipedia.org/wiki/ActionScript' },
            { name: 'ActionScript 2.0', description: 'Secondary programing language to support older flash games', link: 'https://en.wikipedia.org/wiki/ActionScript' },
            { name: 'Node.js', description: 'Used for server to generate scripts', link: 'https://nodejs.org/en/' }
        ]" />
    </div>
</template>