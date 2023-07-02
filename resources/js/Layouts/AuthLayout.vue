<script setup>
import ApplicationLogo from "@/Components/ApplicationLogo.vue";
import { Link } from "@inertiajs/vue3";
</script>

<template>
    <div
        class="h-screen flex justify-center items-center bg-cover w-full"
        style="background-image: url('/img/auth/balloon-lg.jpg')"
    >
        <div
            class="w-full h-auto sm:w-3/4 flex flex-col sm:flex-row m-2 bg-white shadow-md overflow-hidden rounded-lg"
        >
            <div
                class="bg-cover w-full h-2/5 text-left text-white p-4"
                style="background-image: url('/img/auth/balloon-sm.jpg')"
            >
                <h1 class="text-2xl">ALUMNI TRACER PORTAL</h1>
                <p class="text-md text-ellipsis overflow-hidden w-4/5">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Asperiores ipsam voluptatibus laboriosam. Eum unde
                    repudiandae consequatur reiciendis illo rem possimus!
                </p>
            </div>

            <div class="p-4 space-y-4">
                <img src="/img/atu-logo.png" alt="" class="h-14 mr-auto" />
                <slot />
            </div>
        </div>
    </div>
</template>
