<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div style="display: -webkit-box; margin-left: auto; margin-right: auto; width: 300px;">
      <input type="text" id="txtName">
      <div id="btnOk" v-on:click="btnClick">ok</div>
    </div>
    
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
  beforeDestroy (){
    clearInterval(this.intervalid1)
  },
  methods : {
    teste(){          
      this.intervalid1 = setInterval(() => {
          this.alteracoes = Math.floor((Math.random() * 10) + 1);
          // console.log (this.alteracoes);
      }, 1000);
    },
    btnClick(){
      alert(document.getElementById("txtName").value);
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


#btnOk{
  width: 60px;
  height: 25px;
  border-radius: 5px;
  border: 1px solid #ccd8e4;
  color: #4d6a87;
  cursor: pointer;
  margin-left: 10px;
}

#btnOk:hover{
  background-color: #f2f2f2;
}
</style>
