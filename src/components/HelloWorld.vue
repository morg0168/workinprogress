<template>
  <div class="hello" >
    <img @click="setBackgroundImg(bgImgs, counter)" ref="image" v-bind:src="currentImage" />
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'oh hii',
      counter: 0,
      bgImgs: ['logo', 'logo2', 'logo3', 'logo4'],
      currentImage: './static/img/logo2.png'
    }
  },
  mounted: {
//    currentImage: function () {
  //    return setBackgroundImg(bgImgs, counter)
   // }
  },
  methods: {
    setBackgroundImg (bgImgs, counter) {
      var randomNum = Math.floor(Math.random() * bgImgs.length)
      counter = randomNum
      console.log(bgImgs[counter])
     // this.currentImage = './static/' + bgImgs[counter] + '.png'
      this.currentImage = './static/img/' + bgImgs[counter] + '.png';
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
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
.hello {
  height:100vh;
  width:100vw;
}
body {
  background:black;
  width:100%;
  height:100%;
}
img {
  min-height:100vh;
  min-width:100vw;
  z-index:99;
  position:absolute;
  left:0;
  top:0;
}
h1 {
  color:yellow;
  font-weight:800;
  color:yellow;
}
</style>
