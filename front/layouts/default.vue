<template class="gb">
  <v-app dark>
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
    >
      <v-toolbar-title v-text="title" />
      <v-spacer/>
      <v-toolbar-title v-text="title" />
      <v-toolbar-title v-text="title" />
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-navigation-drawer
      v-model="rightDrawer"
      :right="right"
      temporary
      fixed
    >
      <v-list>
        <v-list-item @click.native="right = !right">
          <v-list-item-action>
            <v-icon light>
              mdi-repeat
            </v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch drawer (click me)</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-footer
      :absolute="!fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Top',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Charactor',
          to: '/charactor'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Career',
          to: '/career'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Article',
          to: '/article'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'N.T',
      title2: "aaa"
    }
  }
}
</script>

<style scoped>
  .gb {
    background-image: url("~@/assets/image/bg-dark.jpg");
  }
</style>
