<template>
    <footer class="footer">
        <div class="footer-container">
            <!-- Logo e descrição -->
            <div class="footer-logo">
                <i class="fa fa-tv logo-icon"></i>
                <div>
                    <h2>IPTVOz</h2>
                </div>
            </div>

            <!-- Links rápidos -->
            <div class="footer-links">
                <h3>Links Rápidos</h3>
                <ul>
                    <li><a href="#inicio">Início</a></li>
                    <li><a href="#planos">Planos</a></li>
                    <li><a href="#sobre">Sobre</a></li>
                    <li><a href="#suporte">Suporte</a></li>
                    <li><a href="#contato">Contato</a></li>
                </ul>
            </div>

            <!-- Redes Sociais -->
            <div class="footer-social">
                <h3>Nos siga nas redes</h3>
                <div class="social-icons">
                    <a href="https://wa.link/nqe2ja" target="_blank"><i class="fa-brands fa-whatsapp"></i></a>
                    <a href="#"><i class="fa-brands fa-facebook"></i></a>
                    <a href="#"><i class="fa-brands fa-instagram"></i></a>
                </div>
            </div>
        </div>

        <!-- Linha separadora -->
        <div class="footer-divider"></div>

        <!-- Direitos autorais -->
        <div class="footer-bottom">
            <p>&copy; 2025 IPTVOz. Todos os direitos reservados.</p>
        </div>
    </footer>
</template>

<script>
export default {
    name: "FooterIptv",
};
</script>

<style scoped>

.footer {
    background: #0b1622;
    color: #fff;
    padding: 40px 20px;
    text-align: center;
    font-family: Arial, sans-serif;
}

.footer-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: flex-start;
    max-width: 1000px;
    margin: 0 auto;
    text-align: left;
    width: 100%;
}

.footer-logo {
    display: flex;
    align-items: center;
    gap: 8px;
    font-family: var(--fonte-h1);
    line-height: normal;
    max-width: 250px;
}

.logo-icon {
    font-size: 1.5rem;
    color: var(--cor-primaria);
    line-height: normal;
}

.footer-logo h2 {
    margin: 0;
    font-size: 20px;
}

.footer-links h3,
.footer-social h3 {
    font-size: 16px;
    margin-bottom: 10px;
    font-weight: bold;
}

.footer-links ul {
    list-style: none;
    padding: 0;
}

.footer-links ul li {
    margin-bottom: 8px;
}

.footer-links ul li a {
    text-decoration: none;
    color: #bbb;
    font-size: 14px;
}

.footer-links ul li a:hover {
    color: var(--cor-primaria);
}

.footer-social {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
}

.social-icons {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
}

.social-icons a {
    width: 100%;
    color: #bbb;
    font-size: 1.5rem;
    text-decoration: none;
    transition: color 0.3s;
}

.social-icons a:hover {
    color: #28d07e;
    transition: color 0.3s;
}

.footer-divider {
    width: 100%;
    height: 1px;
    background: #222;
    margin: 20px 0;
}

.footer-bottom {
    font-size: 14px;
    color: #bbb;
}

@media (max-width: 768px) {
    .footer-container {
        flex-direction: column;
        align-items: center;
        text-align: center;
    }

    .footer-logo,
    .footer-links,
    .footer-social {
        align-items: center;
        margin-bottom: 20px;
    }

    .footer-social {
        flex-direction: column;
    }
}
</style>
