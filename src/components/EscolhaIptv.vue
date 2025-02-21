<template>
    <section class="escolha">
        <h2>ESCOLHA</h2>
        <div class="escolha-caixa">
            <div class="escolha-item">
                <i class="escolha-icone fa fa-globe" aria-hidden="true"></i>
                <p class="escolha-texto">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorem illum a beatae!
                </p>
            </div>

            <div class="escolha-item">
                <i class="escolha-icone fa fa-wifi" aria-hidden="true"></i>
                <p class="escolha-texto">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorem illum a beatae!
                </p>
            </div>

            <div class="escolha-item">
                <i class="escolha-icone fa fa-television" aria-hidden="true"></i>
                <p class="escolha-texto">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorem illum a beatae!
                </p>
            </div>
        </div>
    </section>
</template>


<script>
export default {
    name: 'EscolhaIptv'
}
</script>

<style scoped>
.escolha {
    display: flex;
    flex-direction: column;
    min-height: 55vh;
    background-color: var(--cor-fundo);
    justify-content: center;
    align-items: center;
}

h2{
    color: #fff;
    font-family: var(--fonte-titulo) ;
    font-size: 2rem;
    margin-bottom: 1%;
}

.escolha-caixa{
    width: 80%;
    display: flex;
    gap: 20px;

}

.escolha-item{
    width: 50%;
    align-items: center;
    text-align: center;
    padding: 5%;
    background-color: var(--cor-fundo-secundaria);
    border: 2px solid var(--cor-fundo);
    font-size: 1.3rem;
    border-radius: 20px;
}

.escolha-icone{
    font-size: 1.7rem;
    color: var(--cor-icons-1);
    margin-bottom: 7%;
}

.escolha-texto{
    color: #fff;
    font-family: var(--fonte-texto);
}

@media (max-width: 768px) {
    .escolha-caixa {
        flex-direction: column;
        align-items: center;
        gap: 10px;
    }

    .escolha-item {
        width: 80%;
    }
}

@media (max-width: 480px) {
    h2 {
        font-size: 2rem;
    }

    .escolha-icone {
        font-size: 1.5rem;
        line-height: normal;
    }

    .escolha-texto {
        font-size: 1rem;
    }
}
</style>