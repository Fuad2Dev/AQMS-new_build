<script setup>
import { Head } from "@inertiajs/vue3";
import NavBar from "../Components/NavBar.vue";
import Section from "@/Components/Section.vue";
import SectionItem from "@/Components/SectionItem.vue";
import { ref } from "vue";
import SectionGroup from "@/Components/SectionGroup.vue";

const toggleState = ref(0);
const showStatBar = ref(true);
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
        <div class="h-5/6 relative">
            <!-- side bar 1 -->
            <div
                class="absolute w-full h-full bg-transparent flex drop-shadow-xl"
            >
                <div
                    class="w-0 bg-white h-auto overflow-y-auto transition-all duration-300 border-r"
                    :class="{
                        '!w-1/4': toggleState === 1 || toggleState === 2,
                    }"
                >
                    <Section icon="iconsminds-check" name="Surveys" />
                    <Section icon="iconsminds-check" name="Surveys" />
                </div>
                <!-- side bar 2 -->
                <div
                    class="w-0 bg-white overflow-y-auto transition-all duration-300 border-r space-y-3"
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

            <main>
                <p>
                    Lorem, ipsum dolor sit amet consectetur adipisicing elit.
                    Rem eligendi eos, voluptate tempora molestiae iusto, dolorum
                    deserunt voluptatibus nulla, aliquid tenetur corrupti
                    architecto. Quis eum eaque, quam tenetur non nostrum.
                </p>
            </main>

            <div
                class="absolute right-0 top-0 border w-full h-full bg-transparent"
            >
                <div
                    class="relative border w-0 h-full ml-auto bg-white transition-all space-y-8 duration-300"
                    :class="{ 'w-1/2 p-4': showStatBar }"
                >
                <!-- stat bar toggle -->
                    <div 
                        class="absolute h-8 w-8 right-full top-2 bg-white flex justify-center items-center text-xl"
                        @click="showStatBar = !showStatBar"
                    >
                        <div class="simple-icon-star"></div>
                    </div>

                    <div class="space-y-4">
                        <p class="text-xs font-light text-gray-400">Status</p>

                        <div class="space-y-2 text-sm">
                            <div class="flex justify-between">
                                <div class="simple-icon-star"></div>
                                <p>Active Surveys</p>
                                <div>12</div>
                            </div>
                            <div class="flex justify-between">
                                <div class="simple-icon-star"></div>
                                <p>Active Surveys</p>
                                <div>12</div>
                            </div>
                        </div>
                    </div>

                    <div class="space-y-4">
                        <p class="text-xs font-light text-gray-400">Categories</p>
                        
                        <div class="space-y-2 text-sm">
                            <div class="flex ">
                                <input type="checkbox" name="" id="" class="rounded mr-4" />
                                <p>Active Surveys</p>
                            </div>
                            <div class="flex ">
                                <input type="checkbox" name="" id="" class="rounded mr-4" />
                                <p>Active Surveys</p>
                            </div>
                            <div class="flex ">
                                <input type="checkbox" name="" id="" class="rounded mr-4" />
                                <p>Active Surveys</p>
                            </div>
                            
                        </div>
                    </div>
                    

                    <div class="space-y-4">
                        <p class="text-xs font-light text-gray-400">Labels</p>

                        <div class="space-y-2 text-sm">
                            <div>
                                <div class="border border-blue-500 rounded-lg w-fit px-2">
                                    New Framework
                                </div>
                            </div>
                            <div>
                                <div class="border border-blue-500 rounded-lg w-fit px-2">
                                    Education
                                </div>
                            </div>
                            <div>
                                <div class="border border-blue-500 rounded-lg w-fit px-2">
                                    Personal
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
