<template>
    <a href="https://wa.link/nqe2ja" target="_blank" class="botao-teste">Teste Gratuito</a>
</template>

<script>
export default {
    name: 'BotaoIptv',
}
</script>

<style scoped>
.botao-teste {
    background-color: var(--cor-primaria);
    color: var(--cor-fundo);
    padding: 10px 5vw; 
    border-radius: 999px;
    font-weight: 600;
    text-decoration: none;
    transition: background-color 0.3s;
    font-family: var(--fonte-texto);
    font-size: clamp(14px, 1.2vw, 18px); 
    display: inline-block;
    text-align: center;
    max-width: 90%; 
    white-space: nowrap; 
}

.botao-teste:hover {
    background-color: var(--cor-secundaria);
}

/* Ajustes para telas menores */
@media (max-width: 600px) {
    .botao-teste {
        padding: 12px 8vw;
        font-size: 16px;
    }
}
</style>
