<template>
  <div class="flex justify-between max-w-6xl mx-auto py-8">
    <!-- Navigation -->
    <pre>{{ navigation }}</pre>
    <div class="text-white dark:text-gray-200">
      <h3 class="text-3xl font-semibold">
        <NuxtLink to="/" class="mr-6" active-class="font-bold text-orange-600 underline">Home</NuxtLink>
        <ContentNavigation v-slot="{ navigation }">
          <NuxtLink
            v-for="link of navigation"
            :key="link._path"
            :to="link._path"
            active-class="font-bold text-orange-600 underline"
            class="mr-6"
          >
            {{ link.navTitle || link.title }}
          </NuxtLink>
        </ContentNavigation>
      </h3>
    </div>
    <!-- Social icons & Color Mode -->
    <div class="space-x-3 text-gray-500 transition">
      <a href="https://github.com/fabsoftwareitp" title="GitHub" class="hover:text-gray-700 dark:hover:text-gray-300"><Icon name="fa-brands:github" /></a>
      <ColorModeSwitch class="hover:text-gray-700 dark:hover:text-gray-300" />
    </div>
  </div>
</template>
