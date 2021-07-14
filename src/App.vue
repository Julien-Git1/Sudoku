<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <Grid :table="matrice" />
</template>

<script>
/*import HelloWorldVue from "./components/HelloWorld.vue";*/
import Grid from "./components/Grid.vue";
export default {
  name: "App",
  components: {
    /*HelloWorld: HelloWorldVue,*/
    Grid: Grid,
  },
  data() {
    return {
      matrice: test()
    }
  }
};

var initmatrice = [
      { id: 1, ligne: [1,2,3,4,5,6,7,8,9] },
      { id: 2, ligne: [1,2,3,4,5,6,7,8,9] },
      { id: 3, ligne: [1,2,3,4,5,6,7,8,9] },
      { id: 4, ligne: [1,2,3,4,5,6,7,8,9] },
      { id: 5, ligne: [1,2,3,4,5,6,7,8,9] },
      { id: 6, ligne: [1,2,3,4,5,6,7,8,9] },
      { id: 7, ligne: [1,2,3,4,5,6,7,8,9] },
      { id: 8, ligne: [1,2,3,4,5,6,7,8,9] },
      { id: 9, ligne: [1,2,3,4,5,6,7,8,9] }
    ]

function test(){
  let initmatrice1 = shuffle(initmatrice)
  return initmatrice1
}

function shuffle(array) {
  var currentIndex = array.length,  randomIndex;

  // While there remain elements to shuffle...
  while (0 !== currentIndex) {

    // Pick a remaining element...
    randomIndex = Math.floor(Math.random() * currentIndex);
    currentIndex--;

    // And swap it with the current element.
    [array[currentIndex], array[randomIndex]] = [
      array[randomIndex], array[currentIndex]];
  }

  return array;
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
