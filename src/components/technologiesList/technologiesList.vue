<script lang="ts">
import type { PropType } from "vue";
import "./technologiesList.css";

type Item = {
    name: string,
    description: string,
    link: string
}

export default {
    props: {
        items: { type: Object as PropType<Item[]>, required: true }
    }
}
</script>

<template>
    <div class="technologies_list">
        <h3>Technologies</h3>
        <ul>
            <li v-for="item in items">
                <a :href="item.link" target="_blank">
                    {{ item.name }}
                </a>
                {{ item.description }}
            </li>
        </ul>
    </div>
</template>