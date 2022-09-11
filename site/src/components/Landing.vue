<template>
    <section id="who-are-you">
        <h2 id="who-are-you-title">Le concept</h2>
        <div class="who-are-you-content">
            <div class="speech">
                <p>
                    Nous sommes l’unique incubateur-formateur de Paris Panthéon-Assas Université, ouvert à toutes et tous. <br />
                    One Panthéon s'adresse à tous ceux qui souhaitent apprendre, approfondir leurs compétences, imaginer de nouveaux concepts toujours dans un objectif d'enseignement et de partage.<br />
                    Droit, informatique, sciences, photographie, sport… Il n’existe pas de profil particulier pour intégrer One Panthéon. <br />
                    <strong>Qu’attendez-vous donc pour participer à cette expérience unique ?</strong>
                </p>
            </div>
            <div class="logo">
                <img src="/assets/Logo1P.png" alt="Logo One Panthéon" />
                <img src="/assets/LogoEfrei.png" alt="Logo EFREI" />
            </div>
        </div>
    </section>
</template>

<script>
export default {

}
</script>

<style>
    #who-are-you {
        width: 70%;
        margin: auto;
        padding-top: 70px;
        margin-top: -70px;            
    }

    h2 {
        text-align: center;
        font-weight: 500;
        font-size: 34px;
        text-decoration: underline;
        margin: 35px auto 25px;
    }
    
    .who-are-you-content {
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        gap: 100px;
    }

    .who-are-you-content p {
        font-size: 20px;
    }

    strong {
        font-size: 24px;
    }

    .logo {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 20px;
    }

    .logo img {
        height: 125px;
        width: auto;
    }

    @media all and (max-width: 1100px) {
        .who-are-you-content {
            flex-direction: column-reverse;
            gap: 25px;
        }

        .logo img {
            height: auto;
            width: 200px;
        }

        .logo img:last-child {
            margin-bottom: 20px;
        }
    }
</style>