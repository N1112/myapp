<template>
  <v-row>
    <v-col class="text-center">
      <img src="/v.png" alt="Vuetify.js" class="mb-5" />
      <blockquote class="blockquote">
        <div class="profile-name">Nanami Takahashi</div>

        <v-spacer class="space"></v-spacer>

        <div class="profile-title">BirthDay</div>

        <v-spacer class="profile-space"></v-spacer>

        <div class="profile-body">1997/11</div>

        <v-spacer class="space"></v-spacer>

        <div class="profile-title">Adress</div>

        <v-spacer class="profile-space"></v-spacer>

        <div class="profile-body">Tokyo</div>

        <v-spacer class="space"></v-spacer>

        <div class="profile-title">Skill</div>

        <v-spacer class="profile-space"></v-spacer>

        <div class="profile-body">
          <span class="font-red">HTML</span> / <span class="font-red">CSS</span> / <span class="font-red">JavaScript</span> / 
          <span class="font-red">Node.js</span> / <span class="font-red">Vue.js</span> / <span class="font-red">Nuxt.js</span> / TypeScript
          <br />
          PHP / Laravel / MySQL / Docker / Git / Swagger / Stoplight
        </div>

        <v-spacer class="space"></v-spacer>

        <div class="profile-title">Hobby</div>

        <v-spacer class="profile-space"></v-spacer>

        <div class="profile-body">Music / Game / Movie</div>

        <v-spacer class="space"></v-spacer>

        <div class="profile-title">Food</div>

        <v-spacer class="profile-space"></v-spacer>

        <div class="profile-body">Hamburger</div>

        <v-spacer class="profile-space"></v-spacer>
      </blockquote>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: "AboutPage",
};
</script>

<style scoped>
  .space {
    padding-top: 6em;
  }
  .profile-name {
    font-size: 4.5em;
    font-family: Impact;
    padding-top: 1em;
  }
  .profile-space {
    padding-top: 1.5em;
  }
  .profile-title {
    font-size: 3em;
    font-family: Impact;
  }
  .profile-body {
    font-size: 1.3em;
    font-family: Tahoma;
  }
  .font-red {
    color: red;
  }
</style>
