<template>
  <div class="home">
    <boxesInfo :title="msg" :description="description" />
  </div>
</template>

<script>
import boxesInfo from "../components/Boxes.vue"

export default {
  name: 'HomeView',
  data() {
    return {
      msg: "Aproveite na TV.",
      description: "Assista em Smart TVs, PlayStation, Xbox, Chromecast, Apple TV, aparelhos de Blu-ray e outros dispositivos.",
    }
  },
  components: {
    boxesInfo
  }
}
</script>
