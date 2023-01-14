<script lang="ts">
import ProfilePicture from '../profilePicture/ProfilePicture.vue';


export default {
    components: { ProfilePicture }
}
</script>

<template>
    <div class="header_grid">
        <div class="main_cell centered_vertically">
            <h1>Tobias Rheindorf</h1>
            <h4>AKA notSafeForDev</h4>
            <h4>Frontend & Game Developer</h4>
        </div>
        <div>
            <ProfilePicture image-url="portrait.jpg" />
        </div>
    </div>
    <div>
        <div class="spacer_medium"></div>
        <p>I'm Tobias Rheindorf, a developer that really gives it all for exciting projects!</p>
        <p>This site was built from scratch, as a fully responsive website using the <a href="https://vuejs.org/">Vue
                Framework</a>.</p>
    </div>
</template>