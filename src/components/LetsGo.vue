<template>
    <div id="card-form">
        <p>Pronto para assistir? Informe seu email para criar ou reiniciar sua assinatura.</p>
        <div id="inputs">
            <input type="email" :placeholder="email">
            <input type="submit" :value="valor">
        </div>
        <!--inputs-->
    </div>
    <!--card-form-->
</template>

<script>
export default {
    name: "LetsGo",
    data() {
        return {
            email: "Email",
            valor: "Vamos lá >"
        }
    }
}
</script>

<style scoped>

    #card-form {
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        width: 55%;
        text-align: center;
        margin-bottom: 15px;
    }

    #card-form {
        margin-top: 20px;
        margin-bottom: 100px;
        flex-direction: column;
    }

    #card-form p {
        font-size: 1.2rem;
        color: white;
    }

    #inputs {  
        margin-top: 20px;
        width: 100%;
    }

    #inputs input[type=email] {
        max-width: 460px;
        width: 100%;
        height: 60px;
        padding-left: 20px;
        outline: none;
        font-size: 1.2rem;
    }

    #inputs input[type=submit] {
        max-width: 180px;
        width: 100%;
        height: 60px;
        background-color: #e50914;
        color: #fff;
        border: none;
        font-size: 1.2rem;
        cursor: pointer;
        font-weight: bold;
    }

    @media  screen and (max-width: 1160px) {
        #navbar #card-text #inputs input[type=email] {
            width: 60%;
        }

        #navbar #card-text #inputs input[type=submit] {
            width: 30%;
        }
    }

    @media  screen and (max-width: 920px) {
        #navbar #card-text #inputs {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        #navbar #card-text #inputs input[type=email] {
            width: 100%;
        }

        #navbar #card-text #inputs input[type=submit] {
            width: 100%;
            height: 40px;
            margin-top: 20px;
        }
    }
</style>