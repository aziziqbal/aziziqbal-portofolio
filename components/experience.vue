<template>
  <section id="experience" class="hide-overflow">
    <v-layout style="height:100vh;background-color:#303030;">
      <!-- <v-img v-bind:src="'data:image/jpeg;base64,'+imageBytes" class="gambar"> -->
      <!-- </v-img> -->
      <v-row style="z-index:1" class="pa-md-5 pa-3 mx-0">
        <v-col cols="12" style="margin-top:5vh;">
          <h2 data-aos="fade-right" class="font-weight-bold display-2" style="color:#FFAA00;">
            Where I've been
          </h2>
        </v-col>
        <v-col v-show="tampil" cols="12">
          <v-timeline data-aos="fade-left">
            <v-timeline-item color="#ffaa00" v-for="item in data" :key="item.tahun">
              <span slot="opposite" style="font-family:robotobold;">{{ item.tahun }}</span>
              <v-card class="elevation-2">
                <v-card-title class="headline" style="font-weight:420;">{{ item.tempat }}</v-card-title>
                <v-card-subtitle class="subtitle" style="padding-bottom:5px;color:white;">{{ item.posisi }}</v-card-subtitle>
                <v-card-text>
                  {{ item.detail }}
                </v-card-text>
              </v-card>
            </v-timeline-item>
          </v-timeline>
        </v-col>
        <v-col v-show="!tampil" cols="12">
          <v-timeline dense>
            <v-slide-x-reverse-transition
              group
              hide-on-leave
            >
              <v-timeline-item
                v-for="item in data"
                :key="item.tahun"
                color="#ffaa00"
                small
              >
                <v-alert class="white--text">
                  <v-card class="elevation-2">
                    <v-card-title class="" style="font-weight:420;font-size:16px;">{{ item.tempat }}</v-card-title>
                    <v-card-subtitle class="" style="padding-bottom:5px;color:white;font-size:14px;">{{ item.posisi }}</v-card-subtitle>
                    <v-card-text style="font-size:15px;">
                      <!-- {{ item.detail }} -->
                    </v-card-text>
                  </v-card>
                </v-alert>
              </v-timeline-item>
            </v-slide-x-reverse-transition>
          </v-timeline>
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
      data: [
        {
          tahun : '2017 - 2018',
          tempat : 'Embedded System Engineer',
          posisi: 'Agency for the Assessment and Application of Technology (BPPT)',
          detail: 'BPPT is an Indonesian government research institute, which has the tasks of carrying out government duties in the field of assessment and application of technology, and prioritizes the partnership through maximum utilization of technology and engineering outputs.'
        },
        {
          tahun : '2018 - 2019',
          tempat : 'Front End Web Developer',
          posisi : 'Olsera Indonesia Pratama',
          detail: 'Olsera is an unified POS and online store solution for Indonesia SMEs. We simplify offline business process, while also enabling business owners to benefits from online sales.'
        },
        {
          tahun : '2019 - Now',
          tempat : 'Front End Web Developer',
          posisi : 'Widya Inovasi Indonesia',
          detail: 'Widya is a Information and Technology company with solutions that focus on Artificial Intelligence, Automation and Robotics.'
        },
        {
          tahun : '2020 - Now',
          tempat : 'Founder',
          posisi: 'Diffable Academy',
          detail: 'Difabel Academy is a social organization located in Yogyakarta, Indonesia with a focus on providing better education for people with disabilities'
        },
      ],
      window: {
        width: 0,
        height: 0
      },
      tampil: true
    }
  },
  created() {
    window.addEventListener('resize', this.handleResize);
    this.handleResize();
  },
  destroyed() {
    window.removeEventListener('resize', this.handleResize);
  },
  methods: {
    handleResize() {
      this.window.width = window.innerWidth
      this.window.height = window.innerHeight
      if (this.window.width < 1024) {
        this.tampil = false
      } else {
        this.tampil = true
      }
    }
  }
}
</script>
<style scoped>
  .gambar {
    position: absolute!important;
    left: -48px;
    top: 96vh;
    z-index: 0!important;
  }
  @font-face {
    font-family: roboto;
    src: url(../static/Roboto-Light.ttf) format("truetype");
  }
  @font-face {
    font-family: robotobold;
    src: url(../static/Roboto-Bold.ttf) format("truetype");
  }
  .aziz {
    font-family: roboto;
  }
</style>
