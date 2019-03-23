<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    
  </div>
</template>

<script>




export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App ',
    }
  },
  computed:{
    alteracoes : {
      get(){
          return this.msg;
      },
      set(v){
          this.msg =  v;
      }
    }
  },
  mounted : function(){
    this.teste()     
  },
  beforeDestroy () {
    clearInterval(this.intervalid1)
  },
  methods : {
    teste(){          
      this.intervalid1 = setInterval(() => {
          this.alteracoes = Math.floor((Math.random() * 10) + 1);
          // console.log (this.alteracoes);
      }, 1000);
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
