<template>
  <v-app style="{background: $vuetify.theme.themes.dark.brackround}">
    <sideBar/>
    <sideBarRight/>
  </v-app>
</template>

<script>
  import SideBar from '../components/SideBar'
  import SideBarRight from '../components/SideBarRight'

  export default {
    name: 'Home',

    components: {
      SideBar,
      SideBarRight
    }
  }
</script>
