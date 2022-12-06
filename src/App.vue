<template>
  <div class="container">
    <!-- #3 must use the component-->
    <MyHeader mytitle="Playstation games" 
      aboutpage ="List of Games" />
    
    <GamesBox :playstation = "playstation"/>
    <AboutMe aboutme="About" />
    



  </div>
</template>
<script>



//import HelloWorld from './components/HelloWorld.vue'
// 1
import MyHeader from './components/MyHeader.vue'
import AboutMe from './components/AboutMe.vue'
// ----import Bookbox from './components/Bookbox.vue'
import GamesBox from './components/GamesBox.vue'


// data url: http://localhost:5555/gameslist , this might be different for you
export default {
  name: 'App',
  components: {
    // 2 register the component 
    MyHeader,
    GamesBox,
    AboutMe
  },

  data(){
    return {
      playstation: []
    }
  },
  methods: {
    // promises

      async fetchGames(){
         const res= await fetch('https://priyanka-games.herokuapp.com/api')
         const data= await res.json()
          console.log(data)
         return data.playstation
      }

  },

  async created(){
    this.playstation = await this.fetchGames()
  }
}
</script>










<style>




@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
  background-color: #8a8d91;
}
.container {
  max-width: 400px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
  background-color: #aeecef;
}

div{
  margin-bottom: 0.5em;
}



</style>


