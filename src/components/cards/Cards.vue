<script setup>
import { computed } from "vue";
import Database from "../../database.json"


</script>


<template>
  <main class="cardsMain">    
    <section v-for="(item, index) in Database" :key="index" class="card">
        <div class="imageFrame">

        </div>

        <div class="info">
            <h2>{{item.popularNome}}</h2>
            <h3>{{item.especie}}</h3>            

        </div>        
    </section>    
  </main>  
</template>


<style scoped>
.cardsMain{    
    width: 860px;
    display: flex;
    flex-direction: column;  
}
.card{
    margin-bottom: 20px;

    display: flex;
    flex-direction: row;
}

.imageFrame{
    width: 132px;
    height: 132px;

    background-color: gray;
    border-radius: 15px;

    overflow: hidden;
    z-index: 1;
}
.info{
    width: 860px;
    height: 132px;

    background-color: #D9E3ED;
    border-radius: 15px;

    position: absolute;
}

h2{
    margin: 5px 0px 0px 150px;
    font-weight: 400;
}
h3{
    margin: 0px 0px 0px 150px;
    font-weight: 300;
    font-style: italic;
}
</style>
