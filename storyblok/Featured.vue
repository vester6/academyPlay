<template>
    <div v-editable="blok">
        <div>
            <h1> {{ blok.name }} </h1>
        </div>
    </div>
</template>

<script setup>
defineProps({ blok: Object })
</script>