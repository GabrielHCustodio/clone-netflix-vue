<template>
    <div id="box-question">
        <h1>{{ msg }}</h1>
        <ul class="faq-li">
            <li v-for="i in lista" :key="i.id">
                <button id="button" @click.prevent="exibirResposta = !exibirResposta" @mouseover="passado()">
                    <span v-if="exibirResposta">{{ i.questions }} <p>+</p></span>
                    <span v-if="!exibirResposta">{{ i.questions }} <p>x</p></span>
                </button>
                <p id="resposta" v-if="!exibirResposta">{{ i.answers }}</p>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: "PerguntasFaq",
    data() {
        return {
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
                }
            ]
        }
    }
}
</script>

<style scoped>
    #box-question {
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        background-color: black;
        border-bottom: 8px solid #222;
        padding-bottom: 70px;
    }

    #box-question h1 {
        color: white;
        font-size: 50px;
        margin-top: 70px;
    }

    #box-question .faq-li {
        margin-top: 50px;
        width: 50%;
        display: flex;
        justify-content: space-around;
        list-style-type: none;
    }

    #box-question .faq-li li {
        width: 100%;   
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
        height: 300px;
        border-top: 1px solid black;
        color: white;
        padding: 20px;
        font-size: 27px;
    }
</style>