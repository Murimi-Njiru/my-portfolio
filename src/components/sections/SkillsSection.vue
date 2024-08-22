<template>
  <div id="skills-section" class="w-full flex flex-wrap mt-4 p-4">
    <h3 class="text-3xl font-bold dark:text-white mb-4 w-full">Skills</h3>
    <div class="w-full flex flex-wrap md:w-1/3 border-b md:border-r md:border-b-0 border-gray-400 px-2">
      <h3 class="text-lg font-semibold text-gray-900 dark:text-white w-full underline">Programming Languages</h3>
      <div class="grid grid-cols-2 gap-4 w-full">
        <div v-for="(item, index) in programmingLanguages" :key="index" class="flex flex-col justify-center items-center p-2">
          <img :src="item.icon" class="w-12 h-12 transition-all duration-300  cursor-pointer filter md:grayscale hover:grayscale-0" alt="icon">
          <p class="text-sm text-center">{{ item.label }}</p>
        </div>
      </div>
    </div>
    <div class="w-full flex flex-wrap md:w-1/3 border-b md:border-r md:border-b-0 border-gray-400 px-2 pt-2">
      <h3 class="text-lg font-semibold text-gray-900 dark:text-white w-full underline">Libraries</h3>
      <div class="grid grid-cols-2 gap-4 w-full">
        <div v-for="(item, index) in libraries" :key="index" class="flex flex-col justify-center items-center p-2">
          <img :src="item.icon" class="w-12 h-12 transition-all duration-300  cursor-pointer filter md:grayscale hover:grayscale-0" alt="icon">
          <p class="text-sm text-center">{{ item.label }}</p>
        </div>
      </div>
    </div>
    <div class="w-full flex flex-wrap md:w-1/3 px-2 pt-2">
      <h3 class="text-lg font-semibold text-gray-900 dark:text-white w-full underline">Tools</h3>
      <div class="grid grid-cols-2 gap-4 w-full">
        <div v-for="(item, index) in tools" :key="index" class="flex flex-col justify-center items-center p-2">
          <img :src="item.icon" class="w-12 h-12 transition-all duration-300  cursor-pointer filter md:grayscale hover:grayscale-0" alt="icon">
          <p class="text-sm text-center">{{ item.label }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
  export default {
    name: 'SkillsSection',
    data() {
      return {
        programmingLanguages: [
          {
            label: "Javascript",
            icon: require('../../assets/icons/js.png'),
          },
          {
            label: "Java",
            icon: require("../../assets/icons/java.png"),
          },
          {
            label: "Php",
            icon: require("../../assets/icons/php.png"),
          },
          {
            label: "Python",
            icon: require("../../assets/icons/python.png"),
          },
        ],
        libraries: [
          {
            label: "Spring Boot",
            icon: require("../../assets/icons/spring-boot.png"),
          },
          {
            label: "React",
            icon: require("../../assets/icons/react.png"),
          },
          {
            label: "Vue",
            icon: require("../../assets/icons/vue.png"),
          },
          {
            label: "Next",
            icon: require("../../assets/icons/nextjs.png"),
          },
          {
            label: "Lit",
            icon: require("../../assets/icons/js.png"),
          },
          {
            label: "Android",
            icon: require("../../assets/icons/android.png"),
          },
          {
            label: "laravel",
            icon: require("../../assets/icons/laravel.png"),
          }
        ],
        tools: [
          {
            label: "Git",
            icon: require("../../assets/icons/git.png"),
          },
          {
            label: "Github",
            icon: require("../../assets/icons/github.png"),
          },
          {
            label: "Docker",
            icon: require("../../assets/icons/docker.png"),
          },
          {
            label: "Postgres",
            icon: require("../../assets/icons/postgres.png"),
          },
          {
            label: "Nginx",
            icon: require("../../assets/icons/nginx.png"),
          },
          {
            label: "Liquibase",
            icon: require("../../assets/icons/liquibase.png"),
          },
          {
            label: "Redis",
            icon: require("../../assets/icons/redis.png"),
          },
          {
            label: "Microsoft SQL Server",
            icon: require("../../assets/icons/mssql.svg"),
          }
        ]
      }
    }
  }
</script>