<template>
  <div class="max-w-3xl px-4 mx-auto">
    <!-- Header -->
    <Header class="mt-8 mb-4 flex justify-between items-end">
      <div>
        <h1 class="text-2xl font-semibold">
          <!-- 跳轉至首頁/ -->
          <NuxtLink to="/">Personal Blog</NuxtLink>
        </h1>
        <p class="text-gray-500">Learn programming easily</p>
      </div>

      <Btn>Contact/Hire me</Btn>
    </Header>

    <!-- Main content -->
    <!-- 以pages目錄內的index.vue 為主頁-->
    <NuxtPage />
  </div>
</template>
