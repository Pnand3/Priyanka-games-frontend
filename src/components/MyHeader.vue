<template>
<div>
    <h1> {{mytitle}} </h1>
    <h4> {{aboutpage}} </h4>
</div>
</template>

<script>

export default{
    name: 'MyHeader',
    props:{
        mytitle: String,
        aboutpage:String
    }
}

</script>

<style scoped>

div{
    text-align: center;
}

</style>