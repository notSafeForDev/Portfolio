<script lang="ts">
import MobileGame from '../mobileGame/mobileGame.vue';

export default {
    components: { MobileGame }
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
        <p>We ended up releasing Coco Roll on iOS and Android. Whereas Snake+ stayed in the prototype stages.</p>
        <div class="spacer_small"></div>
        <h3>Technologies</h3>
        <ul>
            <li><a href="https://unity.com/">Unity</a>2D & 3D game engine</li>
            <li><a href="https://reactjs.org/">Csharp</a>Programming language</li>
            <li><a href="https://ephtracy.github.io/">MagicaVoxel</a>Voxel based 3D modeling software</li>
            <li><a href="https://www.adobe.com/se/products/animate.html">Adobe Animate</a>Used for creating 2D art and
                animations</li>
        </ul>
    </div>
</template>