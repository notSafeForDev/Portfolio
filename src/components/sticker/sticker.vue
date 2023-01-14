<script lang="ts">
import "./sticker.css";
export default {
    props: {
        text: { type: String, required: true }
    }
}
</script>

<template>
    <div class="sticker">
        <span>{{ text }}</span>
    </div>
</template>