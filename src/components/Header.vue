<template>
    <v-toolbar fixed="true">
    <v-toolbar-side-icon></v-toolbar-side-icon>
    <v-toolbar-title><i class="fab fa-earlybirds fa-2x">YONGHYUN</i></v-toolbar-title>
    <v-spacer></v-spacer>
    <v-toolbar-items class="hidden-sm-and-down">
      <v-btn flat>Link One</v-btn>
      <v-btn flat>Link Two</v-btn>
      <v-btn flat>Link Three</v-btn>
    </v-toolbar-items>
  </v-toolbar>
</template>

<script>
export default {
    name : 'Header',
    components : {

    }
}
</script>