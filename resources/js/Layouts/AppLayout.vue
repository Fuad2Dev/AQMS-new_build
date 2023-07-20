<script setup>
import { Head } from "@inertiajs/vue3";
import NavBar from "../Components/NavBar.vue";
import SideBar from "@/Partials/SideBar.vue"
import StatBar from "@/Partials/StatBar.vue"
import { ref } from "vue";

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

    <div class="h-screen w-screen overflow-x-hidden">
        <NavBar @toggle-side-bar="handleToggle" />
        <div class="h-5/6 relative">

            <SideBar :toggleState="toggleState" />

            <main>
                <p>
                    Lorem, ipsum dolor sit amet consectetur adipisicing elit.
                    Rem eligendi eos, voluptate tempora molestiae iusto, dolorum
                    deserunt voluptatibus nulla, aliquid tenetur corrupti
                    architecto. Quis eum eaque, quam tenetur non nostrum.
                </p>
            </main>

            <StatBar :showStatBar="showStatBar"/>
        </div>
    </div>
</template>
