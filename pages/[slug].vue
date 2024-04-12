<script lang="ts" setup>
// 取得Url中name參數，寫法一
// const route = useRoute();
// const blabla = route.params.name

// 取得Url中name參數，寫法二
const { slug } = useRoute().params;
</script>

<template>
    <div>
        {{ slug }}
    </div>
</template>



<style></style>