<script setup lang="ts">

</script>

<template>
    <div class="">
        <ContentList path="/posts" v-slot="{list}">
            <div v-for="(post, index) in list" :key="post.path" class="blog-cart bg-white rounded-2xl overflow-hidden mb-4">
                {{ post }}
            </div>
        </ContentList>
    </div>
</template>