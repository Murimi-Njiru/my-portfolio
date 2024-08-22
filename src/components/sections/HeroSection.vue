<template>
  <div id="hero-section" class="w-full flex flex-wrap min-h-screen px-3">
    <div class="w-full md:w-1/2 flex flex-col justify-center">
      <h1 class="mb-4 text-4xl text-left  font-extrabold leading-none tracking-tight text-gray-900 md:text-5xl lg:text-6xl dark:text-white">Hi, I'm {{name}}</h1>
      <h5 class="mb-6 text-lg text-left  font-normal text-gray-500 lg:text-xl dark:text-gray-400">{{ message }} </h5>
    </div>
    <div class="w-full md:w-1/2 flex justify-center">
      <img :src="image" class="h-3/4 max-w-lg transition-all duration-300  cursor-pointer filter grayscale hover:grayscale-0" alt="me">
    </div>
  </div>  
</template>

<script>
export default {
  name: 'HeroSection',
  data() {
      return {
        name: "Murimi Njiru Ndwiga",
        message: "and I'm a web developer.",
        image: "../assets/images/me.png"
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