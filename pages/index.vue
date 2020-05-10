<template>
  <div>
    <!-- <v-snackbar v-model="show" :color="color" top right :vertical="vertical">
      <h3 style="margin-bottom:10px;"><b>Info</b></h3>
      Website is under construction !
      <v-btn text @click="show = false">Close</v-btn>
    </v-snackbar> -->
    <home />
    <about />
    <services />
    <experience />
    <skill />
    <portofolio />
    <clients />
    <contact />
  </div>
</template>

<script>
import Home from '~/components/home.vue'
import About from '~/components/about.vue'
import Services from '~/components/services.vue'
import Experience from '~/components/experience.vue'
import Portofolio from '~/components/portofolio.vue'
import Skill from '~/components/skilleducation.vue'
import Contact from '~/components/contacs.vue'
import Clients from '~/components/Clients.vue'

export default {
  components: {
    Home,
    About,
    Services,
    Experience,
    Clients,
    Skill,
    Contact,
    Portofolio,
  },
  data() {
    return {
      show: true,
      vertical: true,
      message: '',
      color: 'red darken-1',
      zIndex: 0,
      zIndex2: 10
    }
  }
}
</script>
<style scoped>
  /* .main-container{
    position: absolute;
    right: 0px;
    top: 0px;
    z-index: -1;
    background-image:url("../assets/full.jpg");
    background-size: cover;
    background-repeat: no-repeat;
    width:100%;
  } */
</style>
