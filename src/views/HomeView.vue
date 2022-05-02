<template>
  <div class="home">
    <NavbarNetflix />
    <boxesInfo 
      v-for="(b , index) in boxes" :key="index"
      :title="b.msg" :description="b.description" :img="b.url" />
    <PerguntasFaq />
    <FooterNetflix/>
  </div>
</template>

<script>
import boxesInfo from "../components/Boxes.vue"
import PerguntasFaq from "../components/Perguntas.vue"
import NavbarNetflix from "../components/Navbar.vue"
import FooterNetflix from "../components/Footer.vue"

export default {
  name: 'HomeView',
  data() {
    return {
      boxes: [{
          msg: "Aproveite na TV.",
          description: "Assista em Smart TVs, PlayStation, Xbox, Chromecast, Apple TV, aparelhos de Blu-ray e outros dispositivos.",
          url :"/image/tv.png" 
        },
        {
          msg: "Baixe séries para assistir offline.",
          description: "Salve seus títulos favoritos e sempre tenha algo para assistir.",
          url :"/image/mobile.jpg"
        },
        {
          msg: "Assista quando quiser.",
          description: "Assista no celular, tablet, Smart TV ou notebook sem pagar a mais por isso.",
          url :"/image/mac.png" 
        },
        {
          msg: "Crie perfis para crianças.",
          description: "Deixe as crianças se aventurarem com seus personagens favoritos em um espaço feito só para elas, sem pagar a mais por isso.",
          url :"/image/kids.png"
        }
      ]
    }
  },
  components: {
    boxesInfo,
    PerguntasFaq,
    NavbarNetflix,
    FooterNetflix
  }
}
</script>