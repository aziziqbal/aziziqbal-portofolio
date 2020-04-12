<template>
  <div class="main-container">
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
import About from '~/components/about.vue'
import Services from '~/components/services.vue'
import Experience from '~/components/experience.vue'
import Portofolio from '~/components/portofolio.vue'
import Skill from '~/components/skilleducation.vue'
import Contact from '~/components/contacs.vue'
import Clients from '~/components/Clients.vue'

export default {
  components: {
    About,
    Services,
    Clients,
    Skill,
    Contact,
    Portofolio,
    Experience
  },
  data() {
    return {
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
