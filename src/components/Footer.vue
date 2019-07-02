<template>
    <v-footer
    dark
    height="auto"
  >
    <v-card
      class="flex"
      flat
      tile
    >
      <v-card-title class="teal">
        <strong class="subheading">주소 : 경기도 김포시 장기동 청송마을 302동 101호</strong>
        <v-spacer></v-spacer>
           <strong class="subheading">연락처 : 010-2876-0585</strong>

        <v-spacer></v-spacer>

        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-3"
          dark
          icon
        >
          <v-icon size="24px">{{ icon }}</v-icon>
        </v-btn>
      </v-card-title>

      <v-card-actions class="grey darken-3 justify-center">
        &copy;2019 — <strong>Vuetify</strong>
      </v-card-actions>
    </v-card>
  </v-footer>
</template>






<script>
export default {
    name : 'Footer',
    components : {

    },
    data() {
      return {
        icons: [
        'fab fa-facebook',
        'fab fa-twitter',
        'fab fa-google-plus',
        'fab fa-linkedin',
        'fab fa-instagram'
      ]
      }
    }
}
</script>