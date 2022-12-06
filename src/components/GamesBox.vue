<template>
    
    <div class="psgames">
        
        <div>
            <GamesDetails :playstation="playstation"/>
     
               
                
                
        
        </div>
       
    </div>

</template>

<script>

import GamesDetails from './GamesDetails.vue'
export default{

    name: 'GamesBox',
    components: {
        GamesDetails
    },
    props: {
        playstation: Array
    }
}

</script>

<style scoped>

.psgames{

    background-color:#26449e;
    padding: 1em;
    color: rgb(51, 58, 145);
}

</style>
