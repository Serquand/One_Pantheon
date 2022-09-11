<template>
    <header class="header-bar-main-container">
        <div class="header-bar-container">
            <div class="logo-container">
                <img src="/assets/Logo1P.png" alt="Logo One Panthéon" />
                <h1>One Panthéon</h1>
            </div>
            <nav class="nav-container">
                <ul>
                    <li>
                        <a 
                        :class="currentSection == 'who' ? 'active' : ''"
                            href="#who-are-you">Présentation</a>
                    </li>
                    
                    <li>
                        <a 
                        :class="currentSection == 'services' ? 'active' : ''"
                            href="#services"
                        >
                            <span class="nos-huge-device">Nos services</span>
                            <span class="nos-little-device">Services</span>
                        </a>
                    </li>

                    <li>
                        <a 
                            :class="currentSection == 'training' ? 'active' : ''" 
                            href="#training"
                        >
                            <span class="nos-huge-device">Nos formations</span>
                            <span class="nos-little-device">Formations</span>
                        </a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
import { ref } from 'vue'

export default {
    setup() {
        const currentSection = ref("")
        return { currentSection }
    },

    mounted() {
        const observer = new IntersectionObserver(entries => {
            entries.forEach(entry => {
                if(entry.intersectionRatio > 0) {
                    const section = entry.target.getAttribute("id")
                    if(section === null || section === undefined) return 
                    this.currentSection = section.split("-")[0]
                }
            })
        }, { rootMargin: '0px 0px -20% 0px' })
        
        document.querySelectorAll("h2").forEach(titleSection => observer.observe(titleSection))
    }
}
</script>

<style scoped>
    .nos-huge-device {
        display: inline;
    }

    .nos-little-device {
        display: none;
    }

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

    .nav-container ul a:hover::after, .active::after {
        animation: appUnderlineHovering 0.2s linear 1 forwards;
    }

    @keyframes appUnderlineHovering {
        from { width: 0%; } 
        to { width: 100%; }
    }

    @media all and (max-width: 900px) {
        .header-bar-container {
            width: 90%;
        }
    }

    @media all and (max-width: 700px) {
        .header-bar-container {
            width: calc(100% - 10px);
        }

        .nav-container ul {
            gap: 5px;
        }

        h1 {
            display: none;
        }

        ul li a {
            font-size: 10px;
        }

        .logo-container img {
            width: 30px;
        }
        
        .nos-huge-device {
            display: none;
        }

        .nos-little-device {
            display: inline;
        }
    }
</style>