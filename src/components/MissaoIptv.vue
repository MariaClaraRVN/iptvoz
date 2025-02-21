<template>
    <section class="missao">
        <h2>NOSSA MISSÃO</h2>
        <div class="missao-container">
        <div class="missao-intro">
            <h2 class="missao-titulo">Missão</h2>
            <p class="missao-descricao-p1">
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Officia provident consequuntur quod quo
                temporibus distinctio autem omnis fugit minus, deleniti sequi similique facere libero dicta tempore
                perferendis voluptatum maxime laboriosam!
            </p>
            <p class="missao-descricao-p2">
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Cupiditate fugiat vero ullam aliquam quod
                provident sequi eaque amet, distinctio explicabo, assumenda enim, molestias doloremque rerum recusandae
                dolores omnis? Exercitationem, earum.
            </p>

            <BotaoIptv/>
        </div>

        <div class="missao-cards">
            <div class="missao-cards-cima">
                <div class="missao-card">
                    <i class="icon fa fa-heart" aria-hidden="true"></i>
                    <h5 class="card-titulo">Título aqui1</h5>
                    <p class="card-descricao">Frase aqui Frase aqui Frase aqui Frase aqui Frase aqui</p>
                </div>

                <div class="missao-card">
                    <i class="icon fa fa-users" aria-hidden="true"></i>
                    <h5 class="card-titulo">Título aqui2</h5>
                    <p class="card-descricao">Frase aqui</p>
                </div>
            </div>

            <div class="missao-cards-baixo">
                <div class="missao-card">
                    <i class="icon fa fa-gavel" aria-hidden="true"></i>
                    <h5 class="card-titulo">Título aqui3</h5>
                    <p class="card-descricao">Frase aqui Frase aqui Frase aqui Frase aqui Frase aqui</p>
                </div>

                <div class="missao-card">
                    <i class="icon fa fa-thumbs-up" aria-hidden="true"></i>
                    <h5 class="card-titulo">Título aqui4</h5>
                    <p class="card-descricao">Frase aqui</p>
                </div>
            </div>
        </div>
    </div>
    </section>
</template>

<script>
import BotaoIptv from './BotaoIptv.vue';

export default {
    name: 'MissaoIptv',
    components:{
        BotaoIptv
    }
}
</script>

<style scoped>
.missao {
    align-items: center;
    padding: 3% 5%;
    text-align: center;
    background-color: var(--cor-fundo);
    color: #fff;
}

h2{
    font-family: var(--fonte-h1);
    font-size: 2rem;
}
.missao-container{
    display: flex;
    gap: 1%;
    padding: 1%;
    flex-direction: row;
}

.missao-intro {
    text-align: left;
    max-width: 55%;
}

.missao-titulo {
    font-size: 2em;
    margin-bottom: 10px;
}

.missao-descricao-p1{
    font-size: 1.1em;
    line-height: 1.6;
    margin-bottom: 15px;
    font-family: var(--fonte-texto);
}

.missao-descricao-p2{
    font-size: 1.1em;
    line-height: 1.6;
    margin-bottom: 4%;
    font-family: var(--fonte-texto);
}

.missao-cards {
    display: flex;
    gap: 20px;
    justify-content: center;
    align-items: center;
    margin-top: 1%;
    font-family: var(--fonte-texto);
}

.icon{
    line-height: normal;
    color: var(--cor-icons-1);
}

.missao-cards-cima .missao-cards-baixo{
    max-width: 50%;
}

.missao-card {
    background-color: var(--cor-fundo-secundaria);
    padding: 4%;
    border-radius: 8px;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    text-align: center;
    flex: 1;
    margin-bottom: 4%;
}

.icon {
    font-size: 2em;
    margin-bottom: 10px;
}

.card-titulo {
    font-size: 1.5em;
    font-weight: bold;
    margin-bottom: 10px;
}

.card-descricao {
    font-size: 1.1em;
}

@media (max-width: 768px) {
    .missao-container {
        flex-direction: column;
        align-items: center;
    }

    .missao-intro {
        max-width: 100%;
        text-align: center;
        order: 2;
    }

    .missao-cards {
        flex-direction: column;
        gap: 10px;
    }

    .missao-cards-cima,
    .missao-cards-baixo {
        max-width: 100%;
    }

    .missao-card {
        width: 100%;
        margin-bottom: 10px;
    }
}

@media (max-width: 480px) {
    h2 {
        font-size: 1.5rem;
    }

    .missao-titulo {
        font-size: 1.5em;
    }

    .card-titulo {
        font-size: 1.2em;
    }

    .card-descricao {
        font-size: 1em;
    }

    .icon {
        font-size: 1.5em;
    }
}
</style>