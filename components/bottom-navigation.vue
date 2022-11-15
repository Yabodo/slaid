<script setup lang="ts">

const date = ref(new Date().getFullYear())

</script>

<template>
<footer class="text-gray-600 body-font">
  <div class="container px-5 py-8 mx-auto flex items-center sm:flex-row flex-col">
    <SlaidLogo />
    <p class="text-sm text-gray-500 sm:ml-4 sm:pl-4 sm:border-l-2 sm:border-gray-200 sm:py-2 sm:mt-0 mt-4">© {{ date }} Kaspar Jõeveer —
      <a href="https://linkedin.com/in/bizi" class="text-gray-600 ml-1" rel="noopener noreferrer" target="_blank">@bizi</a>
    </p>
    <span class="inline-flex sm:ml-auto sm:mt-0 mt-4 justify-center sm:justify-start">
      <div class="sm:border-r-2 sm:border-gray-200 md:pr-4 ">
        <a href="/privacy-policy" class="first-letter:underline underline-offset-[-3px] text-gray-500 pr-2">
          Privaatsussätted
        </a>
        <a href="/terms-of-service" class="first-letter:underline underline-offset-[-3px] text-gray-500">
          Kasutustingimused
        </a>
      </div>
      <a href="https://www.facebook.com/slaid.io" target="_blank" class="pt-0.5 ml-3 text-gray-500">
        <svg fill="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-5 h-5" viewBox="0 0 24 24" data-darkreader-inline-fill="" style="--darkreader-inline-fill:currentColor;">
          <path d="M18 2h-3a5 5 0 00-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 011-1h3z"></path>
        </svg>
      </a>
    </span>
  </div>
</footer>
</template>