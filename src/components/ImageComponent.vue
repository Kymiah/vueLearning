<template>
  <div id="imgId" class="image">
     <img :src="nomaDaImagem" alt="Imagem"/>
  </div>
</template>

<script>
export default {
  name: 'ImageComponent',
  data () {
    return {
      nomaDaImagem: require('../assets/logo.png')
    }
  },
  mounted : ()=>{
    this.teste()     
  },
  methods : {
    getRandomColor(){          
      var letters = '0123456789ABCDEF';
      var color = '#';
      for (var i = 0; i < 6; i++) {
        color += letters[Math.floor(Math.random() * 16)];
      }

      console.log('color');
      return color;
    },
    teste(){
      this.intervalid1 = setInterval(() => {
          document.getElementById("imgId").style.backgroundColor = this.getRandomColor();
          // console.log (this.alteracoes);
      }, 500);
    }
  },
}


</script>


<style scoped>

</style>
