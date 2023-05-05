<template>
  <div id="app">
    <v-layout class="overflow-visible" style="height: 56px;">
    <v-bottom-navigation
      v-model="value"
      color="teal"
      grow
    >
      <router-link to="/" custom
      v-slot="{ navigate}">
     
  <v-btn  @click="navigate" role="link">
 <v-icon aria-hidden="false">
  mdi-account
</v-icon>
        Profile
      </v-btn>
  </router-link>    
 <router-link
      to="/contact"
      custom
      v-slot="{ navigate }">
     
  <v-btn  @click="navigate" role="link">
        <v-icon>mdi-heart</v-icon>

        Contact
      </v-btn>
 </router-link>

 <router-link
      to="/project"
      custom
      v-slot="{ navigate }">
      <v-btn  @click="navigate" role="link">
        <v-icon>mdi-map-marker</v-icon>

        Project
      </v-btn>
 </router-link>
    </v-bottom-navigation>
  </v-layout>
    <router-view />
  </div>
</template>

<script>
export default {
   name: 'App',

   data: () => ({
      //
   })
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
 
}
.router-link-exact-active {
  color: blue;
}
</style>