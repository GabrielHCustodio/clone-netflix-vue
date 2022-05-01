<template>
    <div id="box-information">
        <div id="box-question">
            <h1>{{ msg }}</h1>
            <ul class="faq-li" v-for="i in lista" :key="i.id">
                <li>
                    <button id="button" @click.prevent="exibirResposta = !exibirResposta" @mouseover="passado()">
                        <span v-if="exibirResposta">{{ i.questions }} <p>+</p></span>
                        <span v-if="!exibirResposta">{{ i.questions }} <p>x</p></span>
                    </button>
                    <p id="resposta" v-if="!exibirResposta">{{ i.answers }}</p>
                </li>
            </ul>
        </div>
        <LetsGo />
    </div>
</template>

<script>
import LetsGo from "../components/LetsGo.vue"

export default {
    name: "PerguntasFaq",
    components: {
        LetsGo
    },
    data() {
        return {
            email: "Email",
            valor: "Vamos lá >",
            msg: "Perguntas frequentes",
            exibirResposta: true,
            lista: [
                {
                    questions: "O que é a Netflix?",
                    answers: `A Netflix é um serviço de transmissão online que 
                            oferece uma ampla variedade de séries, filmes e documentários 
                            premiados em milhares de aparelhos conectados à internet.
                            Você pode assistir a quantos filmes e séries quiser, quando e 
                            onde quiser, sem comerciais – tudo por um preço mensal bem acessível. 
                            Aqui você sempre encontra novidades. A cada semana, adicionamos novas séries e filmes`
                },
                {
                    questions: "Quanto custa a Netflix?",
                    answers: `Assista à Netflix no seu celular, tablet, Smart TV, notebook ou 
                            aparelho de streaming por uma taxa mensal única. Os planos variam de R$25,90 a R$55,90 por mês. 
                            Sem contrato nem taxas extras.`
                },
                {
                    questions: "Onde posso assistir?",
                    answers: `Assista onde quiser, quando quiser. Faça login com sua conta Netflix 
                            em netflix.com para começar a assistir no computador ou em qualquer aparelho conectado à 
                            Internet compatível com o aplicativo Netflix, como Smart TVs, smartphones, tablets, 
                            aparelhos de streaming e videogames.
                            Você também pode baixar a sua série favorita com o aplicativo Netflix para iOS, Android 
                            ou Windows 10. Use downloads para levar a Netflix para onde quiser sem precisar de 
                            conexão com a Internet. Leve a Netflix com você para qualquer lugar.`
                },
                {
                    questions: "Como faço para cancelar?",
                    answers: `A Netflix é flexível. Não há contratos nem compromissos. 
                            Você pode cancelar a sua conta na internet com apenas dois cliques. 
                            Não há taxa de cancelamento – você pode começar ou encerrar a sua assinatura a
                            qualquer momento.`
                },
                {
                    questions: "O que eu posso assistir na Netflix?",
                    answers: `A Netflix tem um grande catálogo de filmes, documentários, séries, originais Netflix 
                            premiados e muito mais. Assista o quanto quiser, quando quiser.`
                },
                {
                    questions: "A Netflix é adequada para crianças?",
                    answers: `A experiência infantil da Netflix faz parte da sua assinatura para que as crianças se 
                            divirtam em seu próprio espaço com séries e filmes familiares sob a supervisão dos pais.
                            O recurso de controle dos pais, incluso nos perfis para crianças e protegido por PIN, 
                            permite restringir a classificação etária do conteúdo que as crianças podem ver e 
                            bloquear títulos específicos que você não quer que elas assistam.`
                }
            ]
        }
    }
}
</script>

<style scoped>
    #box-information {
        width: 100%;
        border-bottom: 8px solid #222;
        background-color: black;
    }

    #box-question {
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        padding-bottom: 70px;
    }

    #box-question h1 {
        color: white;
        font-size: 50px;
        margin-top: 70px;
    }

    #box-question .faq-li {
        width: 50%;
        display: flex;
        justify-content: space-around;
        list-style-type: none;
    }

    #box-question .faq-li li {
        width: 100%;
        margin-top: 20px;
    }

    #box-question .faq-li #button,
    #box-question .faq-li #resposta {
        width: 100%;
        height: 60px;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        color: white;
        background-color: #222;
        border: none;
        cursor: pointer;
        font-size: 30px;
        padding: 20px 0;
    }

    #box-question .faq-li #button span {
        width: 95%;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
    }

    #box-question .faq-li #resposta {
        height: 100%;
        border-top: 1px solid black;
        color: white;
        padding: 20px;
        font-size: 27px;
    }
    
    #card-form {
        width: 100%;
    }
</style>