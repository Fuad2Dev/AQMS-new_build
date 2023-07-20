<script setup>
const { icon, name } = defineProps(["name", "icon"]);
</script>

<template>
    <div class="flex space-x-3 items-center min-w-max">
        <i :class="icon"></i>
        <span>{{ name }}</span>
    </div>
</template>
