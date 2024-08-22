
<template>
  <ol class="relative text-gray-500 border-s border-gray-200 dark:border-gray-700 dark:text-gray-400 w-full">
    <li class="ms-6 w-full">
      <span class="absolute flex items-center justify-center w-8 h-8 bg-green-200 rounded-full -start-4 ring-4 ring-white dark:ring-gray-900 dark:bg-green-900">
        <svg class="w-3.5 h-3.5 text-green-500 dark:text-green-400" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 12">
          <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 5.917 5.724 10.5 15 1.5"/>
        </svg>
      </span>
      <h2 class="text-left font-medium leading-tight">{{ title }} at {{ at }}</h2>
      <h2 class="text-left text-sm mb-3">{{ from }} to {{ to }}</h2>
      <ul class="max-w-md space-y-1 mb-4 text-gray-500 list-inside dark:text-gray-400">
        <li class="text-left" v-for="(item, index) in description"  :key="index">{{ item }}</li>
      </ul>
    </li>
  </ol>
</template>

<script>
  export default {
    name: 'WorkExperienceItem',
    props: {
      title: String,
      from: String,
      to: String,
      at: String,
      description: Array
    }
  }
</script>
