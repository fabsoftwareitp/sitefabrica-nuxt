<template>
  <div class="flex justify-center py-8">
    <!-- Navigation -->
    <div class="text-white dark:text-gray-200">
        <NuxtLink to="/" class="mr-6" active-class="font-bold text-orange-600 underline">Home</NuxtLink>
        <ContentNavigation v-slot="{ navigation }">
          <NuxtLink
            v-for="link of navigation"
            :key="link._path"
            :to="link._path"
            active-class="font-bold text-orange-600 underline"
            class="mr-6 font-semibold"
          >
            {{ link.navTitle || link.title }}
          </NuxtLink>
        </ContentNavigation>
    </div>
  </div>
    <!-- Social icons & Color Mode -->
    <div class="space-x-3 text-gray-200 transition hidden ">
      <a href="https://github.com/fabsoftwareitp" title="GitHub" class="hover:text-gray-700 dark:hover:text-gray-300"><Icon name="fa-brands:github" /></a>
      <ColorModeSwitch class="hover:text-gray-700 dark:hover:text-gray-300" />
    </div>
</template>
