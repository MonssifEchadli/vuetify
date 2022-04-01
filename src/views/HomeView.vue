<template>
  <div class="home margin10">
    <h1 class="subtitle-1 grey--text">Home</h1>
    <v-container class="my-1">
      <v-card flat color="#eee" class="pa-7">
        <v-expansion-panels>
          <v-expansion-panel v-for="i in 7" :key="i" >
            <v-expansion-panel-header>
              Item #{{i}}
            </v-expansion-panel-header>
            <v-expansion-panel-content>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>
      </v-card>
    </v-container>
    <h1 class="subtitle-1 grey--text">Contact us</h1>
    <v-container class="my-1">
      <v-card flat color="#eee" class="pa-7">
        <v-layout row justify-space-around>
          <v-btn color="pink darken-3 white--text">
            <v-icon left small>mdi-email</v-icon>
            <span>Email</span>
          </v-btn>
          <v-btn color="pink darken-3 white--text">
            <v-icon left small>mdi-email</v-icon>
            <span>LinkedIn</span>
          </v-btn>
          <v-btn color="pink darken-3 white--text">
            <v-icon left small>mdi-email</v-icon>
            <span>Twitter</span>
          </v-btn>
          <v-btn color="pink darken-3 white--text">
            <v-icon left small>mdi-email</v-icon>
            <span>GitHub</span>
          </v-btn>
          <v-btn color="pink darken-3 white--text">
            <v-icon left small>mdi-email</v-icon>
            <span>Phone</span>
          </v-btn>
        </v-layout>
      </v-card>
    </v-container>
    
  </div>
</template>

<script>

export default {
  data() {
        return {
            projects: [
                {id: 1, title: "TITRE", text:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel repellendus veritatis sed ipsam minus ab illo numquam cupiditate officia et, aliquam laudantium consequatur aut reiciendis saepe corrupti vitae, harum laborum?"},
                {id: 2, title: "TITRE", text:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel repellendus veritatis sed ipsam minus ab illo numquam cupiditate officia et, aliquam laudantium consequatur aut reiciendis saepe corrupti vitae, harum laborum?"},
                {id: 3, title: "TITRE", text:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel repellendus veritatis sed ipsam minus ab illo numquam cupiditate officia et, aliquam laudantium consequatur aut reiciendis saepe corrupti vitae, harum laborum?"},
                {id: 4, title: "TITRE", text:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel repellendus veritatis sed ipsam minus ab illo numquam cupiditate officia et, aliquam laudantium consequatur aut reiciendis saepe corrupti vitae, harum laborum?"},
                {id: 5, title: "TITRE", text:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel repellendus veritatis sed ipsam minus ab illo numquam cupiditate officia et, aliquam laudantium consequatur aut reiciendis saepe corrupti vitae, harum laborum?"},
                {id: 6, title: "TITRE", text:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel repellendus veritatis sed ipsam minus ab illo numquam cupiditate officia et, aliquam laudantium consequatur aut reiciendis saepe corrupti vitae, harum laborum?"},
                {id: 7, title: "TITRE", text:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel repellendus veritatis sed ipsam minus ab illo numquam cupiditate officia et, aliquam laudantium consequatur aut reiciendis saepe corrupti vitae, harum laborum?"},
                {id: 8, title: "TITRE", text:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel repellendus veritatis sed ipsam minus ab illo numquam cupiditate officia et, aliquam laudantium consequatur aut reiciendis saepe corrupti vitae, harum laborum?"},
                {id: 9, title: "TITRE", text:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel repellendus veritatis sed ipsam minus ab illo numquam cupiditate officia et, aliquam laudantium consequatur aut reiciendis saepe corrupti vitae, harum laborum?"},
                {id: 10,title: "TITRE", text:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel repellendus veritatis sed ipsam minus ab illo numquam cupiditate officia et, aliquam laudantium consequatur aut reiciendis saepe corrupti vitae, harum laborum?"},
                {id: 11,title: "TITRE", text:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel repellendus veritatis sed ipsam minus ab illo numquam cupiditate officia et, aliquam laudantium consequatur aut reiciendis saepe corrupti vitae, harum laborum?"},
            ]
        }
  }
}
</script>

<style scoped>

</style>