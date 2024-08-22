<template>
  <div id="work-experience-section" class="w-full flex flex-col flex-wrap px-3">
    <h2 class="text-3xl font-bold dark:text-white mb-4">Work Experience</h2>
    <div class="flex flex-wrap">
      <div class="w-full md:w-1/2 pl-6">
        <ol class="relative border-s border-gray-200 dark:border-gray-700">                  
          <li class="mb-10 ms-6" v-for="(item, index) in experience" :key="index">            
            <span class="absolute flex items-center justify-center w-6 h-6 bg-blue-100 rounded-full -start-3 ring-8 ring-white dark:ring-gray-900 dark:bg-blue-900">
              <svg class="w-2.5 h-2.5 text-blue-800 dark:text-blue-300" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 20 20">
                <path d="M20 4a2 2 0 0 0-2-2h-2V1a1 1 0 0 0-2 0v1h-3V1a1 1 0 0 0-2 0v1H6V1a1 1 0 0 0-2 0v1H2a2 2 0 0 0-2 2v2h20V4ZM0 18a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2V8H0v10Zm5-8h10a1 1 0 0 1 0 2H5a1 1 0 0 1 0-2Z"/>
              </svg>
            </span>
            <h3 class="flex items-center mb-1 text-lg font-semibold text-gray-900 dark:text-white">{{ item.title }} at {{ item.at }}</h3>
            <time class="block mb-2 text-sm font-normal leading-none text-gray-400 dark:text-gray-500">{{ item.from }} to {{ item.to }}</time>
            <ul class="max-w-md space-y-1 mb-4 text-gray-500 list-inside dark:text-gray-400">
              <li class="text-left" v-for="(item1, index1) in item.description"  :key="index1">{{ item1 }}</li>
            </ul>
          </li>
        </ol>
      </div>
      <div class="w-full md:w-1/2 hidden md:flex">
        <img src="@/assets/images/Techie.png" class="h-3/4 m-auto max-w-lg transition-all duration-300  cursor-pointer filter" alt="me">
      </div>
    </div>
  </div>  
</template>

<script>

  export default {
    name: 'WorkExperienceSection',
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