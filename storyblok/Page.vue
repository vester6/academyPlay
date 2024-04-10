<template>
    <div v-editable="blok">
        <StoryblokComponent />  
    </div>
</template>

<script setup>
defineProps({ blok: Object })
</script>