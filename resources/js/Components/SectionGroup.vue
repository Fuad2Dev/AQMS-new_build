<script setup>
import SectionItem from "./SectionItem.vue";
import { ref } from "vue";

const drop = ref(false);
</script>
<template>
    <div class="grid grid-cols-4 min-w-max">
        <div class=" col-span-4 grid grid-cols-4">
            <div class="flex">
                <div @click="drop=!drop"
                    class="simple-icon-arrow-right transition flex"
                    :class="{'rotate-90': drop}"
                ></div>
            </div>
            <p class="col-span-3">section</p>
        </div>
        <div
            class=" transition-all overflow-hidden max-h-0 space-y-3 col-span-3 col-start-2"
            :class="{ 'max-h-96 py-3': drop }"
        >
            <SectionItem icon="simple-icon-eye" name="item" />
            <SectionItem icon="simple-icon-eye" name="item" />
            <SectionItem icon="simple-icon-eye" name="item" />
        </div>
    </div>
</template>
