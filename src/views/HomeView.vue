<script setup lang="ts">
import FlashToySyncSection from "@/components/flashToySyncSection/flashToySyncSection.vue";
import MobileGamesSection from "@/components/mobileGamesSection/mobileGamesSection.vue";
import ProfilePicture from "@/components/profilePicture/ProfilePicture.vue";
import SlotGamesSection from "@/components/slotGamesSection/slotGamesSection.vue";
import VideoPlayerSection from "@/components/videoPlayerSection/videoPlayerSection.vue";
</script>

<template>
  <div class="content">
    <div class="header_grid">
      <div class="main_cell centered_vertically">
        <h1>Tobias Rheindorf</h1>
        <h4>Frontend & Game Developer</h4>
      </div>
      <div>
        <ProfilePicture image-url="portrait.jpg" />
      </div>
    </div>
    <div>
      <div class="spacer_large"></div>
      <p>I'm Tobias Rheindorf, a developer that really gives it all for exciting projects!</p>
      <p>This website was built using the Vue framework, as a way to learn the framework.</p>
    </div>
    <SlotGamesSection />
    <MobileGamesSection />
    <VideoPlayerSection />
    <FlashToySyncSection />
    <div class="spacer_large"></div>
  </div>
</template>
