<script lang="ts" setup>
// 取得當前網頁Url中name參數，寫法一
// const route = useRoute();
// const blabla = route.params.name

// 取得當前網頁Url中name參數，寫法二
const { slug } = useRoute().params;
</script>

<template>
    <article class="bg-white rounded-2xl">
        <ContentDoc :path="`/posts/${slug}`" v-slot="{ doc }">
            <!-- Header -->
            <Header>
                <div class="text-center p-5">
                    <h1 class="text-4xl font-semibold">{{ doc.title }}</h1>
                    <div class="text-gray-500 text-sm mt-2">
                        {{ doc.date }}
                    </div>
                </div>
                <img :src="doc.thumbnail" class="w-full h-full object-cover">
            </Header>
            <!-- Content Area -->
            <div class="p-5 content">
                <ContentRenderer :value="doc"></ContentRenderer>
            </div>
        </ContentDoc>
    </article>
</template>



<style>
.content p:not(:last-child),
.content li:not(:last-child),
.content blockquote:not(:last-child),
.content h1:not(:last-child),
.content h2:not(:last-child),
.content h3:not(:last-child),
.content h4:not(:last-child),
.content pre:not(:last-child),
.content table:not(:last-child) {
    @apply mb-4;
}

.content h1 {
    @apply text-3xl font-bold;
}

.content h2 {
    @apply text-2xl font-bold;
}

.content h3 {
    @apply text-xl font-bold;
}

.content h4 {
    @apply text-lg font-bold;
}

.content h5 {
    @apply text-base font-bold;
}
</style>