<script lang="ts">
export default {
    setup() {
        const recaptchaScript = document.createElement("script");
        recaptchaScript.setAttribute(
            "src",
            "https://s.imgur.com/min/embed.js"
        );
        document.head.appendChild(recaptchaScript);
    },

    // mounted() {
    //     const scriptElement: HTMLScriptElement = document.createElement("script");
    //     scriptElement.setAttribute("src", "https://s.imgur.com/min/embed.js");
    //     document.head.appendChild(scriptElement);
    // }
};

</script>

<template>
    <div>
        <blockquote class="imgur-embed-pub" lang="en" data-id="a/lkGZJ4z" data-context="false"><a
                href="//imgur.com/a/lkGZJ4z">Flash Toy Sync V3 Scripting Basics</a></blockquote>
    </div>
</template>