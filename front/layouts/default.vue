<template>
  <v-app dark>
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
    >
      <v-toolbar-title v-text="items.title" class="header-title"/>
      <v-spacer/>
      <v-btn text class="header-menu" to="/">{{items.top}}</v-btn>
      <v-btn text class="header-menu" to="/works">{{items.work}}</v-btn>
      <v-btn text class="header-menu" to="/blog">{{items.blog}}</v-btn>
      <v-btn text class="header-menu" to="/about">{{items.about}}</v-btn>
    </v-app-bar>
    <div class="circle"></div>
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
  },
  mounted() {
    let setProperty;
    const circle = document.querySelector('.circle');

    document.addEventListener('mousemove', function(e){
      setProperty = `translate(${e.clientX}px, ${e.clientY}px`;
      circle.style.transform = setProperty;
    })
}}
</script>

<style scoped>
  .page-enter-active,
  .page-leave-active {
    transition: opacity 1s;
  }
  .page-enter,
  .page-leave-active {
    opacity: 0;
  }
  .gb {
    background-image: url("@/assets/image/black.jpg");
    background-size: cover;
  }
  .header-title {
    font-size: 2em;
    font-family: Impact;
  }
  .header-menu {
    margin-right: 4em;
    font-family: Impact;
  }
  .header-menu:before {
    background-color: transparent;
  }
.circle {
  position: absolute;
  border: 3px solid rgba(251, 255, 136, 0.947);
  color: rgba(251, 255, 136, 0.947);
  border-radius: 50%;
  pointer-events: none;
  width: 25px;
  height: 25px;
  top: -12.5px;
  left: -12.5px;
  transition: transform .25s ease-out;
  z-index: 999;
}
</style>
