<template>
  <NavbarNetflix />
  <router-view/>
</template>


<script>
import NavbarNetflix from "./components/Navbar.vue"

export default {
  components: {
    NavbarNetflix
  }
}
</script>

<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Helvetica;
  }
</style>