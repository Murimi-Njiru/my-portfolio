<template>
  <div class="w-full flex flex-wrap mt-4">
    <h3 class="text-lg font-semibold text-gray-900 dark:text-white w-full">Skills</h3>
    <div class="w-full flex flex-wrap md:w-1/3 border-gray-400 border-r px-3">
      <h3 class="text-lg font-semibold text-gray-900 dark:text-white w-full underline">Programming Languages</h3>

      <div v-for="(item, index) in programmingLanguages" :key="index" class="w-full md:w-1/2 flex flex-col justify-center items-center p-2">
        <img :src="item.icon" class="w-12 h-12" alt="icon">
        <p class="text-sm text-center">{{ item.label }}</p>
      </div>

    </div>
    <div class="w-full flex flex-wrap md:w-1/3 border-gray-400 border-r px-3">
      <h3 class="text-lg font-semibold text-gray-900 dark:text-white w-full underline">Libraries</h3>
      <SkillItem v-for="(item, index) in libraries" :key="index" :label="item.label" :icon="item.icon" />
    </div>
    <div class="w-full flex flex-wrap md:w-1/3 border-gray-400 border-r px-3">
      <h3 class="text-lg font-semibold text-gray-900 dark:text-white w-full underline">Tools</h3>
      <SkillItem v-for="(item, index) in tools" :key="index" :label="item.label" :icon="item.icon" />
    </div>
  </div>
</template>
<script>
  import SkillItem from '../SkillItem.vue';

  export default {
    name: 'SkillsSection',
    components: {
      SkillItem
    },
    data() {
      return {
        programmingLanguages: [
          {
            label: "Javascript",
            icon: "@/assets/icons/js.png",
          },
          {
            label: "Java",
            icon: "../assets/icons/java.png",
          },
          {
            label: "Php",
            icon: "../assets/icons/php.png",
          },
          {
            label: "Python",
            icon: "../assets/icons/python.png",
          },
        ],
        libraries: [
          {
            label: "Spring Boot",
            icon: "../assets/icons/spring-boot.png",
          },
          {
            label: "React",
            icon: "../assets/icons/react.png",
          },
          {
            label: "Vue",
            icon: "../assets/icons/vue.png",
          },
          {
            label: "Next",
            icon: "../assets/icons/nextjs.png",
          },
          {
            label: "Lit",
            icon: "../assets/icons/js.png",
          },
          {
            label: "Android",
            icon: "../assets/icons/android.png",
          },
          {
            label: "laravel",
            icon: "../assets/icons/laravel.png",
          }
        ],
        tools: [
          {
            label: "Git",
            icon: "../assets/icons/git.png",
          },
          {
            label: "Github",
            icon: "../assets/icons/github.png",
          },
          {
            label: "Docker",
            icon: "../assets/icons/docker.png",
          },
          {
            label: "Postgres",
            icon: "../assets/icons/postgres.png",
          },
          {
            label: "Nginx",
            icon: "../assets/icons/nginx.png",
          },
          {
            label: "Liquibase",
            icon: "../assets/icons/liquibase.png",
          },
          {
            label: "Redis",
            icon: "../assets/icons/redis.png",
          },
          {
            label: "Microsoft SQL Server",
            icon: "../assets/icons/mssql.svg",
          }
        ]
      }
    }
  }
</script>