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

            <main class="subordemMain">
                <section class="item1">
                    <input type="checkbox" name="Mysticeti" id="Mysticeti" class="mysticeti" @change="handleCheckboxChange((e) => (e.target.value))">
                    <label for="Mysticeti">Mysticeti</label>
                </section>

                <section class="item2">
                    <input type="checkbox" name="Odontoceti" id="Odontoceti" class="odontoceti">
                    <label for="Odontoceti">Odontoceti</label>
                </section>
            </main>
        </section>

        <section class="aguaFiltro">
            <header class="cabecalhoFiltro">
                <p>Tipo de Água</p>
                <button>Resetar</button>
            </header>

            <main class="aguaMain">
                <section class="item1">
                    <input type="checkbox" name="Doce" id="Doce" class="doce">
                    <label for="Doce">Doce</label>
                </section>

                <section class="item2">
                    <input type="checkbox" name="Salgada" id="Salgada" class="salgada">
                    <label for="Salgada">Salgada</label>
                </section>
            </main>
        </section>

        <section class="barbatanaFiltro">
            <header class="cabecalhoFiltro">
                <p>Barbatana Dorsal</p>
                <button>Resetar</button>
            </header>

            <main class="barbatanaMain">
                <section class="item1">
                    <input type="checkbox" name="Possui" id="Possui" class="possuiBarb">
                    <label for="Possui">Possui</label>
                </section>

                <section class="item2">
                    <input type="checkbox" name="nPossui" id="nPossui" class="NPossuiBarb">
                    <label for="nPossui">Não Possui</label>
                </section>
            </main>
        </section>

        <section class="tamanhoFiltro">
            <header class="cabecalhoFiltro">
                <p>Tamanho Máximo</p>
                <button>Resetar</button>
            </header>

            <main class="tamanhoMain">
                <div class="line">
                    <section class="item1">
                        <input type="checkbox" name="tam05" id="tam05" class="tam05">
                        <label for="tam05">05</label>
                    </section>
                    <section class="item2">
                        <input type="checkbox" name="tam10" id="tam10" class="tam10">
                        <label for="tam10">10</label>
                    </section>
                </div>

                <div class="line">
                    <section class="item1">
                        <input type="checkbox" name="tam15" id="tam15" class="tam15">
                        <label for="tam15">15</label>
                    </section>
                    <section class="item2">
                        <input type="checkbox" name="tam20" id="tam20" class="tam20">
                        <label for="tam20">20</label>
                    </section>
                </div>

                <div class="line3">
                    <section class="item1">
                        <input type="checkbox" name="tam25" id="tam25" class="tam15">
                        <label for="tam25">25</label>
                    </section>
                    <section class="item2">
                        <input type="checkbox" name="tam30" id="tam30" class="tam30">
                        <label for="tam30">30</label>
                    </section>
                </div>
            </main>
        </section>

        <section class="conservacaoFiltro">
            <header class="cabecalhoFiltro">
                <p>Estado de Conservação</p>
                <button>Resetar</button>
            </header>
            
            <main class="conservacaoMain">
                <div class="line">
                    <section class="item1">
                        <input type="checkbox" name="Seguro" id="Seguro" class="seguro">
                        <label for="Seguro">Seguro</label>
                    </section>
                    <section class="item2">
                        <input type="checkbox" name="Risco" id="Risco" class="risco">
                        <label for="Risco">Risco</label>
                    </section>
                </div>

                <div class="line">
                    <section class="item1">
                        <input type="checkbox" name="Vulneravel" id="Vulneravel" class="vulneravel">
                        <label for="Vulneravel">Vulnerável</label>
                    </section>
                    <section class="item2">
                        <input type="checkbox" name="Extinto" id="Extinto" class="extinto">
                        <label for="Extinto">Extinto</label>
                    </section>
                </div>

                <div class="line3">
                    <section class="item1">
                        <input type="checkbox" name="Desconhecido" id="Desconhecido" class="desconhecido">
                        <label for="Desconhecido">Desconhecido</label>
                    </section>
                </div>
            </main>
        </section>
    </main>
</template>


<style scoped>
p{
    margin: 0 0 0 5px;
    height: 25px;

    font-size: 18px;

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
input{
    display: none;
}
input + label:before{
    content: "";
    width: 15px;
    height: 15px;
    margin: auto 5px 5px 5px;
    
    display: inline-block;
    vertical-align: middle;
    
    background-color: #306F9B;
    border: solid 0.5px #306F9B;
    border-radius: 1px;
    transition: 0.2s;    
}
input:checked + label:before{
    content: "";    
    background-color: #D9E3ED;
    transition: 0.2s;    
}

.cabecalho{
    height: 25px;
    margin: 15px 0 20px 0;
    
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

.subordemMain, .aguaMain, .barbatanaMain{
    display: flex;
    flex-direction: row;
    justify-content: space-between;

    margin-bottom: 20px;
    position: relative;
}
.line{
    display: flex;
    flex-direction: row;
    justify-content: space-between;

    margin-bottom: 10px;
    position: relative;
}
.line3{
    display: flex;
    flex-direction: row;
    justify-content: space-between;

    margin-bottom: 20px;
    position: relative;
}
.item1, .item2{
    display: flex;
    flex-direction: row;
    gap: 5px;    
}
.item2{
    position: absolute;
    left: 150px;
}
label{
    font-size: 15px;
    color: #306F9B;
}
</style>