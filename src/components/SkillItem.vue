
<template>
  <div class="w-full md:w-1/2 flex flex-col justify-center items-center p-2">
    <img :src="icon" class="w-12 h-12" alt="icon">
    <p class="text-sm text-center">{{ label }}</p>
  </div>
</template>
<script>
  export default {
    name: 'SkillItem',
    data() {
      return {
        icon1: "../assets/icons/js.png",
      }
    },
    props: {
      label: String,
      icon: String
    }
  }
</script>