<script setup>
import { Head } from "@inertiajs/vue3";
import NavBar from "../Components/NavBar.vue";
import Section from "@/Components/Section.vue";
import SectionItem from "@/Components/SectionItem.vue";
import { ref } from "vue";
import SectionGroup from "@/Components/SectionGroup.vue";

const toggleState = ref(0);
let increaseToggleState = true;

function handleToggle() {
    if (toggleState.value == 1) {
        toggleState.value = increaseToggleState ? 2 : 0;
        increaseToggleState = toggleState.value == 0;
        return;
    }

    toggleState.value = 1;
}
</script>

<template>
    <Head>
        <link rel="stylesheet" href="/icons/iconsminds.css" />
        <link rel="stylesheet" href="/icons/simple-line-icons.css" />
    </Head>

    <div class="h-screen">
        <NavBar @toggle-side-bar="handleToggle" />
        <div class="h-5/6 flex">
            <!-- side bar 1 -->
            <div
                class="w-0 h-auto bg-white overflow-y-auto transition-all border-r"
                :class="{
                    '!w-1/4': toggleState === 1 || toggleState === 2,
                }"
            >
                <Section icon="iconsminds-check" name="Surveys" />
                <Section icon="iconsminds-check" name="Surveys" />
            </div>

            <!-- side bar 2 -->
            <div
                class="w-0 bg-white overflow-y-auto  transition-all border-r space-y-3"
                :class="{
                    'w-2/4 px-6': toggleState === 2,
                }"
            >
                <SectionGroup />
                <SectionGroup />
                <SectionItem icon="simple-icon-eye" name="item" />
                <SectionItem icon="simple-icon-eye" name="item" />
                <SectionItem icon="simple-icon-eye" name="item" /> 
            </div>
        </div>
        
    </div>
</template>
