<template >
  <div id="app">
    <HelloWorld msg="PISIT KHONPAKWAEN" />
    <br>
    <div class="l">
      <counter lable=" " />
    </div>

    <div class="bg badge-pill badge-primary ">
      <br>
      <div class="row">
        <div class="col">
          Name
          <input type="text" class="btn btn-light btn-outline-success" v-model="name" />
        </div>
        <div class="col">
          Code
          <input type="text" class="btn btn-light btn-outline-success" v-model="code" />
        </div>
        <div class="col">
          GPA
          <input type="number" class="btn btn-light btn-outline-success" v-model="gpa" step="0.01" />
        </div>
      </div>
      Name = {{name}}
      <br>
      Code = {{code}}
      <br>
      GPA = {{gpa}}
      

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
      code: "",
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
