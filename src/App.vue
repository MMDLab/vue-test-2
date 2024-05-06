<template>
  <div id="app">

    <img alt="Vue logo" src="./assets/logo.png">

    <p>{{ inputData }}</p>
    <input type="text" v-model="inputData" />
    
    <button @click="onAddInputDatatoList">Click the button</button>

    <ul>
      <li v-for="elem in inputDataArray" :key="elem" >{{elem}}</li>
    </ul>
  
  </div>
</template>

<script>

export default {

  name: 'App',

  data(){
    return {
      inputData:null,
      inputDataArray:[]
    };
  },

  methods:{
    /* *This method adds input data to out array* */
    onAddInputDatatoList(){
      this.inputDataArray.push(this.inputData);
      console.log("the list is", this.inputDataArray)
    }
  },

  components: {
  }
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
