<template>
   
    <div v-for="playstation in playstation" :key="playstation.id">
       <h2>{{playstation.title}}</h2>
       <h4>{{playstation.genre}}</h4>
       <h4>{{playstation.company}}</h4>
       <h4>{{playstation.year}}</h4>
       <h4>{{playstation.rating}} </h4>
    </div>
   
   
   
</template>

<script>

export default{
    name: 'GamesDetails',
    props:{
        playstation: Array
    }
   
}
</script>

<style scoped>

h4{
    margin: 2px;
}


div{
    background-color: #dab7d9;
    color: #17186e;
    padding: 1em;
}



</style>