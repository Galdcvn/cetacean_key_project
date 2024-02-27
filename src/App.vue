<script setup>
import Filtros from "./components/filtros/Filtros.vue"
import Cards from "./components/cards/Cards.vue"
</script>

<template>
  <div class="appScreen">
    <section class="parteCima">
      <main>
        <img src="./assets/logo.svg" alt="Logo" class="logo">
        <input type="text" name="queryBar" class="queryBar">
      </main>     
    </section>

    <section class="parteBaixo">
      <main class="baixoMain">
        <section class="filtros">
          <Filtros />
        </section>

        <section class="cards">
          <h1>ANIMAIS ENCONTRADOS:</h1>
          <Cards />
        </section>
      </main>
    </section>
  </div>  
</template>

<style scoped>
  .appScreen{
    width: 100vw;
    height: 768px;
  }

  .parteCima{
    height: 263px;
    background-color: #306F9B;

    display: flex;
    justify-content: center;
  }
  .parteCima main{
    width: 1200px;

    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 40px;
  }
  .logo{
    margin-top: 5px;
  }
  .queryBar{
    width: 996px;
    height: 46px;

    border-radius: 25px;
    border: none;

    text-align: center;
    font-size: 20pt;
    
    box-shadow: -2px 3px 5px 3px rgba(32,79,113,0.25);
  }

  .parteBaixo{
    height: 505px;

    display: flex;
    justify-content: center;
  }
  .baixoMain{
    width: 1200px;

    display: flex;
   justify-content: space-between;
    gap: 55px;
  }
  .filtros{
    width: 285px;
    overflow-y: scroll;
  }
  .cards{
    width: 860px;
  }
  h1{
    font-weight: 700;
    font-size: 30px;
  }
</style>
