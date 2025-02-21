<template>
    <a href="#" class="botao-teste">Teste Gratuito</a>
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
    padding: 10px 5vw; /* Ajusta dinamicamente o padding */
    border-radius: 999px;
    font-weight: 600;
    text-decoration: none;
    transition: background-color 0.3s;
    font-family: var(--fonte-texto);
    font-size: clamp(14px, 1.2vw, 18px); /* Se adapta entre 14px e 18px */
    display: inline-block;
    text-align: center;
    max-width: 90%; /* Evita botões muito largos */
    white-space: nowrap; /* Evita quebra de linha */
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
