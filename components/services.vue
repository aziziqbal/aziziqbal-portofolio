<template>
  <section id="services" class="hide-overflow">
    <v-layout style="height:100vh;background-color:#303030;">
      <v-img data-aos="fade-left" eager contain class="gambar hidden-sm-and-down" height="130vh"  position="right" :src="require('../assets/aziz5.png')" />
      <v-row style="z-index:1" class="pa-md-5 pa-3 mx-0">
        <v-col cols="12" style="margin-top:5vh;">
          <h2 data-aos="fade-right" class="font-weight-bold display-2" style="color:#FFAA00;">
            What I can do for you.
          </h2>
        </v-col>
        <v-col data-aos="fade-right" cols="12" md="7" style="height:60vh;">
          <v-row class="justify-space-between">
            <v-col cols="12" md="7">
              <v-expansion-panels pop>
                <v-expansion-panel>
                  <v-expansion-panel-header>Web Development</v-expansion-panel-header>
                  <v-expansion-panel-content>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
                  </v-expansion-panel-content>
                </v-expansion-panel>
                <v-expansion-panel>
                  <v-expansion-panel-header>UI / UX Design</v-expansion-panel-header>
                  <v-expansion-panel-content>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
                  </v-expansion-panel-content>
                </v-expansion-panel>
                <v-expansion-panel>
                  <v-expansion-panel-header>Android Development</v-expansion-panel-header>
                  <v-expansion-panel-content>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
                  </v-expansion-panel-content>
                </v-expansion-panel>
                <v-expansion-panel>
                  <v-expansion-panel-header>Internet Of Things</v-expansion-panel-header>
                  <v-expansion-panel-content>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
                  </v-expansion-panel-content>
                </v-expansion-panel>
              </v-expansion-panels>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-layout>
  </section>
</template>
<script>
export default {
  data() {
    return {
      zIndex: 0,
      zIndex2: 1,
      imageBytes: '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'
    }
  }
}
</script>
<style scoped>
  .gambar {
    position: absolute!important;
    right: 0px;
    top: 160vh;
    z-index: 0!important;
  }
  @font-face {
    font-family: roboto;
    src: url(../static/Roboto-Light.ttf) format("truetype");
  }
  .aziz {
    font-family: roboto;
  }
  .warna {
    color:#FFAA00;
  }
  .detail-warna {
  }
</style>
