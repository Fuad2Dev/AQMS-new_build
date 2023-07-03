<script setup>
import ApplicationLogo from "@/Components/ApplicationLogo.vue";
import { Link } from "@inertiajs/vue3";
</script>

<template>
    <div
        class="h-screen flex justify-center items-center bg-cover w-full sm:p-4"
        style="background-image: url('/img/auth/balloon-lg.jpg')"
    >
    <!-- container -->
        <div
            class="w-full h-auto  sm:w-3/4 flex flex-col sm:flex-row m-2  bg-white shadow-md overflow-hidden rounded-lg"
        >
        <!-- left -->
            <div class="w-full sm:w-3/5">
                <div
                    class="bg-cover w-full h-full text-left text-white p-4 space-y-4"
                    style="background-image: url('/img/auth/balloon-sm.jpg')"
                >
                <h1 class="text-2xl font-bold">ALUMNI TRACER PORTAL</h1>
                <p class="text-md text-ellipsis overflow-hidden w-4/5">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Asperiores ipsam voluptatibus laboriosam. Eum unde
                    repudiandae consequatur reiciendis illo rem possimus!
                </p>
            </div>
        </div>
            
        <!-- right -->
            <div class="w-full p-4 sm:w-1/2 md:w-2/5 h-full space-y-4 flex flex-col justify-center">
                <img src="/img/atu-logo.png" alt="" class="h-14 mr-auto" />
                    <slot />
            </div>
        </div>
    </div>
</template>
