<script setup lang="ts">
import FlashToySyncSection from "@/components/flashToySyncSection/flashToySyncSection.vue";
import HeroSection from "@/components/heroSection/heroSection.vue";
import MobileGamesSection from "@/components/mobileGamesSection/mobileGamesSection.vue";
import ProfilePicture from "@/components/profilePicture/ProfilePicture.vue";
import SlotGamesSection from "@/components/slotGamesSection/slotGamesSection.vue";
import VideoPlayerSection from "@/components/videoPlayerSection/videoPlayerSection.vue";
</script>

<template>
  <div class="content">
    <HeroSection />
    <SlotGamesSection />
    <MobileGamesSection />
    <VideoPlayerSection />
    <FlashToySyncSection />
  </div>
</template>
