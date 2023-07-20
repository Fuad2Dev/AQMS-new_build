<script setup>
</script>

<template>
    <nav class="h-1/6 px-8 flex justify-between items-center bg-white">
            <!-- left side -->
            <div class="flex space-x-1" @click="$emit('toggleSideBar')">
                <div class="w-2 space-y-1">
                    <div class="border w-full"></div>
                    <div class="border w-full"></div>
                    <div class="border w-full"></div>
                </div>
                <div class="w-4 space-y-1">
                    <div class="border w-full"></div>
                    <div class="border w-full"></div>
                    <div class="border w-full"></div>
                </div>
            </div>

            <!-- right side -->
            <div class="flex items-center space-x-6">
                <div class="relative">
                    <i class="simple-icon-bell"></i>
                    <div class="z-0 border border-blue-400 rounded-full w-6 h-6 flex justify-center items-center text-xs absolute -top-4 -right-3">99</div>
                </div>
                <p class="hidden sm:block">Fuad Muhammed</p>
                <div class="border rounded-full">
                    <i class="iconsminds-student-male"></i>
                </div>
            </div>
        </nav>
</template>
