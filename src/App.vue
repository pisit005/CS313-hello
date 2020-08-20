<template >
  <div id="app">
    <HelloWorld msg="PISIT KHONPAKWAEN" />
      <div class=" l">
        <counter lable=" "  />
      </div>
  </div>
</template>



<script>
import HelloWorld from "./components/HelloWorld.vue";
import counter from "./components/counter.vue";

export default {

  components: {
    HelloWorld,
    counter,
  },

  data: function () {
    return {
      name: "",
      id: "",
      gpa: "",
    };
  },

};
</script>



<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fafdff;
  margin-top: 30px;
  margin-bottom: 30px;
  font-weight: 800;
  
  

}
</style>
