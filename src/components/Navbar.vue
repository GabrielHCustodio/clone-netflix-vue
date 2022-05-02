<template>
    <div id="navbar">
        <div id="nav">
            <div id="logo_url">
                <img :src="logo" :alt="logo">
            </div><!--logo_url-->
            <div id="informations">
                <select name="" id="language">
                    <option selected lang="pt" data-language="pt" data-country="BR" value="/br/">Português</option>
                    <option lang="en" data-language="en" data-country="BR" value="/br-en/">Inglês</option>
                </select>

                <button id="btn-login">Entrar</button>
            </div><!--language-->
        </div>
        <!--nav-->

        <div id="card-text">
            <div id="card-title">
                <h1>Filmes, séries e muito mais. Sem limites.</h1>
            </div>
            <!--card-title-->
            <div id="card-subtitle">
                <h4>Assista onde quiser. Cancele quando quiser.</h4>
            </div>
            <!--card-subtitle-->
            <LetsGo />
        </div>
        <!--card-text-->
    </div>

</template>

<script>
import LetsGo from "../components/LetsGo.vue"
export default {
    name: "NavbarNetflix",
    components: {
        LetsGo
    },
    data() {
        return {
            logo: '/image/logo.svg'
        }
    }
}
</script>

<style scoped>

    #navbar {
        max-width: 100vw;
        width: 100%;
        height: 100%;
        background: rgba(0, 0, 0, 0.6) url("/public/image/banner.jpg");
        background-size: cover;
        background-repeat: no-repeat;
        border-bottom: 8px solid #222;
        background-blend-mode: darken;
        position: relative;
        display: flex;
        flex-direction: column;
    }

    #navbar #nav {
        width: 100%;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        padding: 25px 50px;
        position: absolute;
    }

    #navbar #nav #logo_url img{
        width: 100%;
        max-width: 130px;
    }

    #navbar #nav #informations {
        display: flex;
        flex-direction: row;
    }

    #navbar #nav #informations #language {
        width: 110px;
        height: 36px;
        margin-right: 30px;
        font-size: 1rem;
        padding-left: 10px;
        color: white;
        background-color: transparent;
        outline: none;
        border: 1px solid #fff;
        border-radius: 3px;
    }

    #navbar #nav #informations #language option {
        color: #fff;
        background-color: #222;
        font-size: 0.9rem;
    }

    #navbar #nav #informations #btn-login {
        width: 80px;
        height: 34px;
        font-size: 16px;
        font-weight: bolder;
        background-color: #e50914;
        color: #fff;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        transition: 0.5s;
    }

    #navbar #nav #informations #btn-login:hover {
        color: #e50914;
        background-color: #fff;
    }

    #navbar #card-text {
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        color: #fff;
        margin-top: -100px;
    }

    #navbar #card-text #card-title,
    #navbar #card-text #card-subtitle {
        display: flex;
        justify-content: center;
        width: 55%;
        text-align: center;
        margin-bottom: 15px;
    }

    #navbar #card-text #card-title h1 {
        margin-top: 55vh;
        font-size: 3.1rem;
    }

    #navbar #card-text #card-subtitle h4 {
        font-size: 1.65rem;
        font-weight: normal;
    }

</style>