<template>
  <v-app dark>
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
    >
      <v-toolbar-title v-text="items.title" />
      <v-spacer/>
      <v-btn text class="header-menu" to="/">{{items.top}}</v-btn>
      <v-btn text class="header-menu" to="/works">{{items.work}}</v-btn>
      <v-btn text class="header-menu" to="/blog">{{items.blog}}</v-btn>
      <v-btn text class="header-menu" to="/about">{{items.about}}</v-btn>
    </v-app-bar>
    <v-main class="gb">
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
    <!-- <v-footer
      :absolute="!fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer> -->
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
      miniVariant: false,
      right: true,
      rightDrawer: false,
      items: {
        title: 'NANAMI.TAKAHASHI',
        top: 'Top',
        work: 'Works',
        blog: 'Blog',
        about: 'About'
      },
    }
  }
}
</script>

<style scoped>
  .gb {
    background-image: url("@/assets/image/black.jpg");
    background-size: cover;
  }
  .header-menu {
    margin-right: 4em;
  }
  .header-menu:before {
    background-color: transparent;
  }
</style>
