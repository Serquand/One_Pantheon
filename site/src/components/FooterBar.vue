<template>
    <footer>
        <div class="footer-main-container">
            <div class="general-container">
                <div class="logo-container">
                    <img src="/assets/Logo1P.png" alt="Logo One Panthéon" />
                    <img src="/assets/LogoEfrei.png" alt="Logo EFREI" />
                </div>
            </div>

            <div class="contact-container">
            <h3>Contact</h3>
                <ul class="footer-ul contact-ul">
                    <li><a :href="'mailto:' + info.contactMail">{{ info.contactMail }}</a></li>
                    <li><a :href="'tel:' + info.numberPhone">{{ info.numberPhoneDisplay }}</a></li>
                    <li><a :href="info.linkedin">{{ info.linkedin }}</a></li>
                    <li><a :href="info.twitter">{{ info.twitter }}</a></li>
                </ul>
            </div>

            <div class="navigation-container">
                <h3>Navigation</h3>
                <nav>
                    <ul class="footer-ul navigation-ul">
                        <li><a href="#">Accueil</a></li>
                        <li><a href="#who-are-you">Qui sommes-nous</a></li>
                        <li><a href="#services">Nos services</a></li>
                        <li><a href="#training">Nos formations</a></li>
                    </ul>
                </nav>
            </div>
        </div>
        <hr />
        <h2>One Panthéon</h2>
    </footer>
</template>

<style scoped>
    footer {
        border-top: 1px solid #333;
        padding: 15px 0;
    }

    .footer-main-container {
        display: flex;
        width: 90%;
        margin: auto;
        justify-content: space-around;
        align-items: flex-start;
    }

    .general-container {
        display: flex;
        flex-direction: column;
    }

    .general-container .logo-container {
        display: flex;
        flex-direction: column;
    }

    .general-container .logo-container img {
        width: 75px;
        height: auto;
    }

    .footer-main-container h3 {
        font-size: 21px;
        font-variant-caps: small-caps;
        font-weight: 500;
        margin-bottom: 7px;
    }

    ul {
        list-style-type: none;
    }

    footer ul li a {
        color: white;
        text-decoration: none;
    }

    footer ul li {
        margin-top: 1px;
    }

    h2 {
        font-size: 20px;
        font-variant-caps: small-caps;
        text-decoration: none;
        font-weight: 500;
        margin: 5px auto 0;
    }

    footer ul li a:hover {
        color: rgb(16, 96, 16);
    }

    hr {
        display: none;
    }

    @media all and (max-width: 650px) {
        .footer-main-container {
            flex-direction: column;
            gap: 40px;
            align-items: flex-start;
            width: min-content;
            margin: auto;
        }   

        .general-container {
            align-self: center;
        }

        hr {
            display: block;
            height: 2px;
            width: 20%;
            color: white;
            margin: 15px auto;
        }
    }
</style>

<script>
import Informations from "../information.json"
export default {
    setup() {
        const info = Informations
        return { info }
    }
}
</script>