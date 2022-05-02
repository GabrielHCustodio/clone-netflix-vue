<template>
    <div id="footer-container">
        <h6>Dúvidas ? Ligue <a href="">9999-999-9999</a></h6>
        <div id="container-links">
            <table>
                <tr>
                    <td>Perguntas frequentes</td>
                    <td>Centro de ajuda</td>
                    <td>Conta</td>
                    <td>Media Center</td>
                </tr>

                <tr>
                    <td>Relações com investidores</td>
                    <td>Carreiras</td>
                    <td>Resgatar cartão pré-pago</td> 
                    <td>Comprar cartão pré-pago</td>   
                </tr>
                
                <tr>
                    <td>Formas de assistir</td>
                    <td>Termos de uso</td>
                    <td>Privacidade</td>
                    <td>Preferências de cookies</td>    
                 </tr>
                
                <tr>
                    <td>Informações corporativas</td>
                    <td>Entre em contato</td>
                    <td>Teste de velocidade</td>
                    <td>Avisos legais</td>
                </tr>

                <tr>
                    <td>Só na Netflix</td>
                </tr>
            </table>
        </div>

        <div id="select-language">
            <select name="" id="language">
                <option selected lang="pt" data-language="pt" data-country="BR" value="/br/">Português</option>
                <option lang="en" data-language="en" data-country="BR" value="/br-en/">Inglês</option>
            </select>
        </div>

        <p>Netflix Brasil</p>
    </div>
</template>

<script>
export default {
    name : "FooterNetflix"
}
</script>

<style scoped>
    #footer-container {
        width: 100%;
        height: 100%;
        background-color: black;
        color: #555;
    }

    #footer-container h6 {
        font-size: 1.1rem;
        font-weight: normal;
        padding: 65px 0 30px 155px;
    }

    #footer-container h6 a {
        text-decoration: none;
        color: #555;
    }

    #footer-container #container-links {
        width: 80%;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    #footer-container #container-links tr {
        font-size: 0.85rem;
    }

    #footer-container #container-links tr td {
        padding-top: 10px;
        padding-left: 60px;
        cursor: pointer;
    }

    #footer-container #select-language {
        padding: 30px 0 30px 155px;
    }

    #footer-container #select-language #language {
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

    #footer-container #select-language #language option {
        color: #fff;
        background-color: #222;
        font-size: 0.9rem;
    }

    #footer-container p {
        padding: 20px 0 30px 155px;
        font-size: 0.9rem;
    }

</style>