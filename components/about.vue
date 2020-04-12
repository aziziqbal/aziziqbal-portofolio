<template>
  <section id="about" class="hide-overflow">
    <v-layout>
      <v-img
        src="https://aziziqbal.com/bg_image/bg_about.jpg"
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
</style>
