<template>
  <section id="home" class="hide-overflow">
    <v-layout>
        <v-img
          src="https://aziziqbal.com/bg_image/42.jpg"
          height="100vh">
          <v-row align="end" justify="end" class="text-right fill-height pa-md-5 pa-3 mx-0">
            <div>
              <p class="aziz text-uppercase font-weight-regular" :class="{'display-1': $vuetify.breakpoint. smAndDown, 'display-3': $vuetify.breakpoint. mdAndUp}">
                Muh Aziz Iqbal
              </p>
              <p class="aziz text-uppercase" :class="{'display-2': $vuetify.breakpoint. smAndDown, 'display-4': $vuetify.breakpoint. mdAndUp}" style="color:#FFAA00;">
                Front-end Developer
              </p>
            </div>
          </v-row>
        </v-img>
        <vue-particles class="hidden-sm-and-down" :moveSpeed="10" color="#dedede"></vue-particles>
    </v-layout>
  </section>
</template>

<style scoped>
  @font-face {
    font-family: roboto;
    src: url(../static/Roboto-Light.ttf) format("truetype");
  }
  .aziz {
    font-family: roboto;
  }
  #particles-js { position: absolute; background-size: cover; top: 0; bottom: 0; left: 0; right: 0; overflow-y: hidden; z-index: 0; }
</style>
