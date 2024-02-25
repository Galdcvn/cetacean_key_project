<script setup>

</script>

<template>
    <header class="cabecalho">
        <p>Filtros</p>
        <button>Resetar</button>
    </header>
    <main class="corpo">
        <section class="subordemFiltro">
            <header class="cabecalhoFiltro">
                <p>Subordem</p>
                <button>Resetar</button>
            </header>

            <main>
                
            </main>
        </section>

        <section class="aguaFiltro">
            <header class="cabecalhoFiltro">
                <p>Tipo de Água</p>
                <button>Resetar</button>
            </header>

            <main>

            </main>
        </section>

        <section class="barbatanaFiltro">
            <header class="cabecalhoFiltro">
                <p>Barbatana Dorsal</p>
                <button>Resetar</button>
            </header>
            <main>


            </main>
        </section>

        <section class="tamanhoFiltro">
            <header class="cabecalhoFiltro">
                <p>Tamanho Máximo</p>
                <button>Resetar</button>
            </header>

            <main>

            </main>
        </section>

        <section class="conservacaoFiltro">
            <header class="cabecalhoFiltro">
                <p>Estado de Conservação</p>
                <button>Resetar</button>
            </header>
            
            <main>

            </main>
        </section>
    </main>
</template>

<style scoped>
p{
    margin: 0 0 0 5px;
    height: 25px;
    font-size: 20px;
    line-height: 20pt;

    color: #0D2738;
}
button{
    height: 25px;
    font-size: 15px;
    
    background: none;
    border: none;
    color: #306F9B;
}
button:hover{
    cursor: pointer;
}

.cabecalho{
    height: 25px;
    margin: 20px 0 15px 0;
    
    display: flex;
    justify-content: space-between;
    align-items: center;

    font-size: 20pt;
}
.corpo header{
    height: 25px;
    margin-bottom: 10px;
    background-color: #D9E3ED;
    border-radius: 5px;

    display: flex;
    justify-content: space-between; 
    align-items: center;   
}
</style>