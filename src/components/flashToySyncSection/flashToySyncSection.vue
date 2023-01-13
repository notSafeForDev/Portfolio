<script lang="ts">
import ImageLink from '../imageLink/imageLink.vue';
import Sticker from '../sticker/sticker.vue';

export default {
    components: { ImageLink, Sticker }
}
</script>

<template>
    <div>
        <div class="black full_width slanted_5 overlap_down_200px highlight_bottom">
            <div class="spacer_large"></div>
        </div>
        <h2>Flash Toy Sync</h2>
        <h3>2020 / 2022</h3>
        <!-- <a title="flash toy sync" href="https://imgur.com/a/lkGZJ4z" target="_blank">
            <div>
                <img src="https://i.imgur.com/loT4QVr.png" />
            </div>
        </a> -->
        <ImageLink title="flash toy sync" href="https://imgur.com/a/lkGZJ4z" src="https://i.imgur.com/loT4QVr.png">
            <Sticker text="ADULT ONLY" />
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
        <a href="https://github.com/notSafeForDev/flash-toy-sync-v3"
            target="_blank">https://github.com/notSafeForDev/flash-toy-sync-v3</a>
        <div class="spacer_small"></div>
        <h3>Technologies</h3>
        <ul>
            <li><a href="https://get.adobe.com/flashplayer/about">Flash</a>Multimedia software platform</li>
            <li><a href="https://en.wikipedia.org/wiki/ActionScript">ActionScript 3.0</a>Primary programing language
            </li>
            <li><a href="https://en.wikipedia.org/wiki/ActionScript">ActionScript 2.0</a>Secondary programing language,
                for supporting AS2 based flash games</li>
            <li><a href="https://nodejs.org/en/">Node.js</a>Used for server to generate scripts</li>
        </ul>
    </div>
</template>