<script setup>
const {icon, name} = defineProps(['icon', 'name'])
</script>

<template>
    <div class="flex flex-col items-center py-3 border-b">
        <i :class="icon" style="font-size: 32px"></i>
        <p>{{ name }}</p>
    </div>
</template>
