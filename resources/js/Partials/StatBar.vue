<template>
    <div class="absolute right-0 top-0 border w-full h-full bg-transparent">
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
                    <div class="flex">
                        <input
                            type="checkbox"
                            name=""
                            id=""
                            class="rounded mr-4"
                        />
                        <p>Active Surveys</p>
                    </div>
                    <div class="flex">
                        <input
                            type="checkbox"
                            name=""
                            id=""
                            class="rounded mr-4"
                        />
                        <p>Active Surveys</p>
                    </div>
                    <div class="flex">
                        <input
                            type="checkbox"
                            name=""
                            id=""
                            class="rounded mr-4"
                        />
                        <p>Active Surveys</p>
                    </div>
                </div>
            </div>

            <div class="space-y-4">
                <p class="text-xs font-light text-gray-400">Labels</p>

                <div class="space-y-2 text-sm">
                    <div>
                        <div
                            class="border border-blue-500 rounded-lg w-fit px-2"
                        >
                            New Framework
                        </div>
                    </div>
                    <div>
                        <div
                            class="border border-blue-500 rounded-lg w-fit px-2"
                        >
                            Education
                        </div>
                    </div>
                    <div>
                        <div
                            class="border border-blue-500 rounded-lg w-fit px-2"
                        >
                            Personal
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
defineProps(['showStatBar'])
</script>
