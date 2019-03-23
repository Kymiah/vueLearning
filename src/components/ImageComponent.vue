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
  }
}

function getRandomColor() {
  var letters = '0123456789ABCDEF';
  var color = '#';
  for (var i = 0; i < 6; i++) {
    color += letters[Math.floor(Math.random() * 16)];
  }
  return color;
}

window.onload = function() {
  var i = setInterval(function(){
    // do your thing
    document.getElementById("imgId").style.backgroundColor = getRandomColor();
}, 200);
  
}


</script>


<style scoped>

</style>
