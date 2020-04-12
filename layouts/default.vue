<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="variant"
      :clipped="clipped"
      fixed
      app
      style="background-color:rgb(24, 24, 24);border-color: rgb(24, 24, 24);overflow-y: hidden;"
    >
      <v-list-item class="text-center">
        <v-list-item-content>
          <v-list-item-title class="title2">
            AI
          </v-list-item-title>
          <v-list-item-title class="nama">
            Muh Aziz Iqbal
          </v-list-item-title>
          <v-list-item-title class="jobs">
            Front-end Developer
          </v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          @click="coba(item)"
          router
          exact
        >
          <v-list-item-content class="text-center">
            <v-list-item-title v-text="item.title" style="font-size:.875rem;"/>
          </v-list-item-content>
        </v-list-item>
      </v-list>
      <template v-slot:append>
        <div class="pa-2 copyright text-center">
          Copyright © 2020 aziziqbal.com
        </div>
      </template>
    </v-navigation-drawer>
    <v-content>
      <v-container style="padding:0px;">
        <nuxt />
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      variant: false,
      drawer: true,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'About Me',
          to: '#about'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Services',
          to: '#services'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Experience',
          to: '#experience'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Skill & Education',
          to: '#skill'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Portofolio',
          to: '#portofolio'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Clients',
          to: '#clients'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Contact',
          to: '#contact'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  },
  methods: {
    coba(item) {
      console.log(item)
      // this.$vuetify.goTo(item.to)
    }
  }
}
</script>
<style scoped>
  @font-face {
    font-family: roboto;
    src: url(../static/Roboto-Light.ttf) format("truetype");
  }
  .title2 {
    font-family: roboto;
    color: #ffaa00 !important;
    caret-color: #ffaa00 !important;
    font-size: 3.75rem!important;
    line-height: 3.75rem;
    letter-spacing: -.0083333333em!important;
    margin-top: 8px!important;
    margin-bottom: 8px!important;
  }
  .nama {
    font-family: roboto;
    color: white;
    font-size: 2.025rem!important;
    line-height: 2.5rem;
    letter-spacing: .0073529412em!important;
    margin-bottom: 8px!important;
  }
  .jobs {
    font-family: roboto;
    color:white;
    font-weight: 300!important;
    font-size: 1.25rem!important;
    letter-spacing: .0125em!important;
  }
  .copyright {
    font-family: roboto;
    color:white;
    font-weight: 300!important;
    font-size: 0.75rem!important;
    letter-spacing: .0125em!important;
  }
</style>
