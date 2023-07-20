<template>
    <div
        class="absolute w-full h-full bg-transparent flex drop-shadow-xl"
        :class="{
            'z-50': toggleState === 1 || toggleState === 2,
        }"
    >
        <!-- left side bar 1 -->
        <div
            class="w-0 bg-white h-auto overflow-y-auto transition-all duration-300 border-r"
            :class="{
                '!w-1/4': toggleState === 1 || toggleState === 2,
            }"
        >
            <Section icon="iconsminds-check" name="Surveys" />
            <Section icon="iconsminds-check" name="Surveys" />
        </div>
        <!-- left side bar 2 -->
        <div
            class="w-0 bg-white overflow-y-auto transition-all duration-300 border-r space-y-3"
            :class="{
                'w-2/4 px-6 z-50': toggleState === 2,
            }"
        >
            <SectionGroup />
            <SectionGroup />
            <SectionItem icon="simple-icon-eye" name="item" />
            <SectionItem icon="simple-icon-eye" name="item" />
            <SectionItem icon="simple-icon-eye" name="item" />
        </div>
    </div>
</template>

<script setup>
defineProps(['toggleState']);
import Section from "@/Components/Section.vue";
import SectionItem from "@/Components/SectionItem.vue";
import SectionGroup from "@/Components/SectionGroup.vue";
</script>
