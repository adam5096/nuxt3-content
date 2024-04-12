<script setup lang="ts">

</script>

<template>
    <div class="">
        <ContentList path="/posts" v-slot="{list}">
            {{ list }}
        </ContentList>
    </div>
</template>