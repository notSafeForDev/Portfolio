<script setup lang="ts">
import ProfilePicture from "@/components/profilePicture/ProfilePicture.vue";
import ImgurEmbed from "@/components/ImgurEmbed/ImgurEmbed.vue";
import "./HomeView.css";
</script>

<template>
  <div class="content">
    <div class="header_grid">
      <div class="main_cell centered_vertically">
        <h1>Tobias Rheindorf</h1>
        <p>Job application For Sweet Tech AS - built using Vue</p>
      </div>
      <div>
        <ProfilePicture image-url="portrait.jpg" />
      </div>
    </div>
    <div>
      <p>
        Hi Alexander, Erik and the others from the Handy team!
        I'm Tobias Rheindorf, a developer that really gives it all for exciting projects!
      </p>
      <div class="black full_width slanted_5 overlap_down_200px highlight_bottom">
        <div class="spacer_100px"></div>
      </div>
      <h2>Flash Toy Sync</h2>
      <a href="https://imgur.com/a/lkGZJ4z" target="_blank"><img src="https://i.imgur.com/loT4QVr.png" /></a>
      <!-- <ImgurEmbed /> -->
      <p>My journey with theHandy started here.</p>
      <p>An application that I built to allow almost any Flash animation found on the net to control theHandy. Built to
        breath
        new life into content that was created in the past decades. And as an homage to the technology that got me into
        development, back in 2005.</p>
      <a
        href="https://github.com/notSafeForDev/flash-toy-sync-v3">https://github.com/notSafeForDev/flash-toy-sync-v3</a>
    </div>

    <!-- <img class="portrait_image" src="@/assets/images/portrait.jpg" /> -->

    <!-- <ProfilePicture :image-url="require(`../assets/images/portrait.jpg`)" /> -->
  </div>
  <!-- <main> -->
  <!-- <TheWelcome /> -->
  <!-- </main> -->
</template>
