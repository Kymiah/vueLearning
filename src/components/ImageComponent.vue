<template>
  <div id="imgId" class="imageBox">
     <img :src="nomaDaImagem" alt="Imagem" class="image"/>
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
  mounted : function (){
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
.image{
  mix-blend-mode: luminosity;
}
</style>
