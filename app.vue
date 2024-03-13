
<script setup>
// get token from runtime config
const { githubToken } = useRuntimeConfig();

// init cookie for github token
const cookie = useCookie("github-token");

// set cookie value if not set
cookie.value = cookie.value || githubToken;
</script>
<template>
  <div class="flex flex-col min-h-screen">
    <SiteHeader/>
    <main class="mx-auto max-w-7xl px-2 sm:px-6 lg:px-8 grow items-start w-full">
      <NuxtPage />
    </main>
    <SiteFooter />
  </div>
</template>
