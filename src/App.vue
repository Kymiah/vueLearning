<template>
  <div id="app">
    <ImageComponent/>
    <HelloWorld/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import ImageComponent from './components/ImageComponent'

export default {
  name: 'App',
  components: {
    HelloWorld,
    ImageComponent
  }
}

</script>

<style>
html{
  background-color: #e9e9e9;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  
}

#imgId{
  transition: 1s;
  -webkit-transition: 1s;
}
</style>
