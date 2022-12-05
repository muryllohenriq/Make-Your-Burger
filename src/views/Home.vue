<template>
  <Banner />
  <div class="main-container">
    <h1>Monte o seu burger:</h1>
    <BurgerForm/>
  </div>
</template>

<script>
import BurgerForm from '@/components/BurgerForm.vue'
import Banner from "../components/Banner.vue"

export default {
  name: "Home",
  components: {
    Banner,
    BurgerForm
  }
}

</script>
