<template>
  <div id="app">
    <div class="w-full min-h-screen">
      <HeroSection />
      <WorkExperienceSection />
      <SkillsSection />
      <!-- <HelloWorld msg="Welcome to Your Vue.js App" name="Vlad" :items="items" /> -->
    </div>
  </div>

</template>

<script>
  import HeroSection from './components/sections/HeroSection.vue';
  import SkillsSection from './components/sections/SkillsSection.vue';
  import WorkExperienceSection from './components/sections/WorkExperienceSection.vue';

  export default {
    name: 'App',
    components: {
      HeroSection,
      WorkExperienceSection,
      SkillsSection
    },
    data() {
      return {
        items: [
          {name: "test", url: "https://google.com"},
          {name: "test2", url: "https://google.com"},
          {name: "test3", url: "https://google.com"}
        ]
      } 
    }
  }
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
  }
</style>
