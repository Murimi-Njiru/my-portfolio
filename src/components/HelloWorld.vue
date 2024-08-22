<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      Rada Rada
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <h3>Installed CLI Plugins</h3>
    <ul>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel" target="_blank" rel="noopener">babel</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint" target="_blank" rel="noopener">eslint</a></li>
    </ul>
    <button id="testBtn" @click="onTestBtnClickHandler">Test</button>
    <h3>Essential Links {{ name ?? "Oops" }}</h3>
    <h3>Essential Links {{ message ?? "Oops" }}</h3>
    <input type="text" v-model="message">
    <ul>
      <li><a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank" rel="noopener">Forum</a></li>
      <li><a href="https://chat.vuejs.org" target="_blank" rel="noopener">Community Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank" rel="noopener">Twitter</a></li>
      <li><a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a></li>
    </ul>
    <h3>Ecosystem</h3>

    <ul>
      <li v-for="(item, index) in items" :key="index"><a :href="item.url" target="_blank" rel="noopener">{{item.name}}</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
    name: String
  },
  data() {
      return {
        message: "Hello World",
        items: [
          {name: "test", url: "https://google.com"},
          {name: "test2", url: "https://google.com"},
          {name: "test3", url: "https://google.com"}
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

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h3 {
    margin: 40px 0 0;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    display: inline-block;
    margin: 0 10px;
  }
  a {
    color: #42b983;
  }
</style>
