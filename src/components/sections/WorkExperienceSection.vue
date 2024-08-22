<template>
  <div id="work-experience-section" class="w-full flex flex-col flex-wrap px-3">
    <h2 class="mb-2 text-lg font-semibold text-gray-900 dark:text-white">Work Experience</h2>
    <div class="flex flex-wrap">
      <div class="w-full md:w-1/2 pl-6">
        <WorkExperienceItem v-for="(item, index) in experience" :key="index" :title="item.title" :from="item.from" :to="item.to" :at="item.at" :description="item.description" />
      </div>
      <div class="w-full md:w-1/2">
        <img src="@/assets/images/Techie.png" class="h-3/4 m-auto max-w-lg transition-all duration-300  cursor-pointer filter" alt="me">
      </div>
    </div>
  </div>  
</template>

<script>
  import WorkExperienceItem from '../WorkExperienceItem.vue';

  export default {
    name: 'WorkExperienceSection',
    components: {
      WorkExperienceItem
    },
    data() {
      return {
        experience: [
        
          {
            title: "Senior Frontend Developer",
            from: "August 2024",
            to: "Present",
            at: "Nathan Digital",
            description: [
              "Test"
            ]
          },
          {
            title: "Full Stack Engineer",
            from: "January 2024",
            to: "August 2024",
            at: "AO Technology Group",
            description: [
              "Developed and maintained applications for our financial clients.",
              "Developed hotel management and Point of Sale applications for our hotel industry clients.",
            ]
          },
          {
            title: "Web Lead",
            from: "December 2022",
            to: "January 2024",
            at: "InterIntel Technologies",
            description: [
              "Lead the entire web team to develop the company’s products.",
              "Designed and developed a new style guide for the company to streamline and harmonize the user interfaces of the web apps.",
              "Developed a new build flow the web applications to improve speed, reduce bundle sizes and improve developer experience of the company's apps."
            ]
          },
          {
            title: "Frontend Developer",
            from: "March 2021",
            to: "December 2022",
            at: "InterIntel Technologies",
            description: [
              "Developed responsive web applications including bulk SMS, inventory management, and a payment gateway that have active users.",
              "Implemented the web applications using Lit.js, a JavaScript library that builds web components that are reusable across other JavaScript libraries because web components are native to browsers hence aren't library specific.",
              "Implemented and designed UI/UX designs using tools like figma."
            ]
          }
        ]
      } 
    },
    methods: {
      onTestBtnClickHandler(e) {
        console.log("Test button clicked" )
        console.log(e);
        
      }
    }
  }
</script>