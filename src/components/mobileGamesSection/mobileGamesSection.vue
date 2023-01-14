<script lang="ts">
import MobileGame from '../mobileGame/mobileGame.vue';
import TechnologiesList from '../technologiesList/technologiesList.vue';

export default {
    components: { MobileGame, TechnologiesList }
}
</script>

<template>
    <div>
        <div class="black full_width slanted_5 overlap_down_200px highlight_bottom">
            <div class="spacer_large"></div>
        </div>
        <h2>Mobile Games</h2>
        <h3>2016 / 2018</h3>
        <div class="grid phone_grid">
            <MobileGame name="Coco Roll" videoUrl="https://www.youtube.com/embed/4LhjYodGJwE"
                artStationUrl="https://www.artstation.com/artwork/orArO" />
            <MobileGame name="Snake+" videoUrl="https://www.youtube.com/embed/2K98kZpM8Mc"
                artStationUrl="https://www.artstation.com/artwork/XB1YBD" />
        </div>
        <p>I studied game design from 2012 to 2015. The following year I started developing mobile phone games along
            with my cousin and a friend of his.</p>
        <p>We ended up releasing Coco Roll for iOS and Android. Whereas Snake+ stayed in the prototype stages.</p>
        <div class="spacer_small"></div>
        <TechnologiesList :items="[
            { name: 'Unity', description: '2D & 3D game engine', link: 'https://unity.com/' },
            { name: 'Csharp', description: 'Programming language', link: 'https://en.wikipedia.org/wiki/C_Sharp_(programming_language)' },
            { name: 'MagicaVoxel', description: 'Voxel based 3D modeling software', link: 'https://ephtracy.github.io/' },
            { name: 'Adobe Animate', description: 'Vector based art and animations software', link: 'https://www.adobe.com/products/animate.html' }
        ]" />
    </div>
</template>