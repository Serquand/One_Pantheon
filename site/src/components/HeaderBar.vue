<template>
    <header class="header-bar-main-container">
        <div class="header-bar-container">
            <div class="logo-container">
                <img src="/assets/Logo1P.png" alt="Logo One Panthéon" />
                <h1>One Panthéon</h1>
            </div>
            <nav class="nav-container">
                <ul>
                    <li><a href="#who-are-you">Présentation</a></li>
                    <li><a href="#services">Nos services</a></li>
                    <li><a href="#training">Nos formations</a></li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
export default {

}
</script>

<style>
    .header-bar-main-container {
        z-index: 1000;
        position: sticky;
        top: 0;
        left: 0;
        background-color: #689fbc;
        color: white !important;
        padding: 10px 0;
        border-bottom: 1px solid #333;
    }

    .header-bar-container {
        width: 70%;
        margin: auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .logo-container {
        display: flex;
        align-items: center;
        gap: 15px;
    }

    .logo-container img {
        width: 45px;
    }

    .logo-container h1 {
        font-variant-caps: small-caps;
        font-weight: 500;
        font-size: 25px;
    }

    .nav-container ul {
        list-style-type: none;
        display: flex;
        gap: 20px;
    }

    .nav-container ul a {
        display: block;
        cursor: pointer;
        color: white;
        text-decoration: none;
        font-size: 17px;
    }

    .nav-container ul a::after {
        height: 1px;
        display: block;
        width: 0%;
        position: relative;
        content: "";
        background-color: white;
    }

    .nav-container ul a:hover::after {
        animation: appUnderlineHovering 0.2s linear 1 forwards;
    }

    @keyframes appUnderlineHovering {
        from {
            width: 0%;
        } 
        to {
            width: 100%;
        }
    }

    @media all and (max-width: 900px) {
        .header-bar-container {
            width: 90%;
        }
    }

    @media all and (max-width: 700px) {
        .header-bar-container {
            width: calc(100% - 20px);
        }

        .nav-container ul {
            gap: 10px;
        }

        h1 {
            display: none;
        }

        ul li a {
            font-size: 15px;
        }

        .logo-container img {
            width: 30px;
        }
    }
</style>