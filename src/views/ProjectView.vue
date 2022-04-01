<template>
  <div class="project margin10">
    <h1 class="subtitle-1 grey--text">My Projects</h1>
    <v-container class="my-5">
      <v-layout row class="mb-5">
        <v-chip @click="sortBy('titre')" close close-icon="mdi-information" color="pink darken-3 white--text mr-3">sort by title</v-chip>
        <v-chip @click="sortBy('text')" close close-icon="mdi-information" color="pink darken-3 white--text mr-3">sort by text</v-chip>
        <v-spacer></v-spacer> <!-- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -->
        <pop-up></pop-up>
      </v-layout>
      <v-card flat color="#eee" class="pa-5">
        <v-layout row justify-space-around>
          <v-flex xs12 md6 lg4 v-for="p in projects" :key="p.id">
            <v-card flat :class="`ma-2 pa-4 ${p.etat}`">
              <h3 class="mb-1">{{ p.titre }}</h3>
              <h5 class="mb-1 grey--text"># {{ p.id }}</h5>
              <p>{{ p.text }}</p>
              <div class="text-right">
                <v-chip close close-icon="mdi-information" color="black--text" :class="`${p.etat}`">
                  Info
                </v-chip>
              </div>
            </v-card>
          </v-flex>
        </v-layout>
      </v-card>
    </v-container>
    
  </div>
</template>

<script>
import PopUp from '../components/PopUp.vue'

export default {
  components: {
    PopUp
  },
  data() {
    return {
      projects: [
        {id: 1, etat: "encour", titre: "title 1", text:"A Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel repellendus veritatis sed ipsam minus ab illo numquam cupiditate officia et, aliquam laudantium consequatur aut reiciendis saepe corrupti vitae, harum laborum?"},
        {id: 2, etat: "termin", titre: "this is a title", text:"C Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel repellendus veritatis sed ipsam minus ab illo numquam cupiditate officia et, aliquam laudantium consequatur aut reiciendis saepe corrupti vitae, harum laborum?"},
        {id: 3, etat: "enatte", titre: "a title", text:"X Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel repellendus veritatis sed ipsam minus ab illo numquam cupiditate officia et, aliquam laudantium consequatur aut reiciendis saepe corrupti vitae, harum laborum?"},
        {id: 4, etat: "termin", titre: "the 4th title", text:"B Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel repellendus veritatis sed ipsam minus ab illo numquam cupiditate officia et, aliquam laudantium consequatur aut reiciendis saepe corrupti vitae, harum laborum?"},
        {id: 5, etat: "enatte", titre: "title n 4", text:"S Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel repellendus veritatis sed ipsam minus ab illo numquam cupiditate officia et, aliquam laudantium consequatur aut reiciendis saepe corrupti vitae, harum laborum?"},
        {id: 6, etat: "encour", titre: "title", text:"M Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel repellendus veritatis sed ipsam minus ab illo numquam cupiditate officia et, aliquam laudantium consequatur aut reiciendis saepe corrupti vitae, harum laborum?"},
        {id: 7, etat: "termin", titre: "t", text:"L Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel repellendus veritatis sed ipsam minus ab illo numquam cupiditate officia et, aliquam laudantium consequatur aut reiciendis saepe corrupti vitae, harum laborum?"},
      ],
      sorted1 : false,
      sorted2 : false,
    }
  },
  methods: {
    sortBy(x) {
      if(x=='titre') {
        if(!this.sorted1) {
          this.projects.sort((a,b) => a[x] < b[x] ? -1 : 1);
        }else {
          this.projects.sort((a,b) => a[x] < b[x] ? 1 : -1);
        }
        this.sorted1 = !this.sorted1;
      } else {
        if(!this.sorted2) {
          this.projects.sort((a,b) => a[x] < b[x] ? -1 : 1);
        }else {
          this.projects.sort((a,b) => a[x] < b[x] ? 1 : -1);
        }
        this.sorted2 = !this.sorted2;
      }
    }
  }
}
</script>

<style scoped>
.termin {
  border-left: 2px solid #3e63;
  border-top: 4px solid #3e63;
}
.encour {
  border-left: 2px solid #ea63;
  border-top: 4px solid #ea63;
}
.enatte {
  border-left: 2px solid #e363;
  border-top: 4px solid #e363;
}
.v-chip {
  border: 0;
}
.v-chip.termin {
  background-color: #3e65 !important;
}
.v-chip.encour {
  background-color: #ea65 !important;
}
.v-chip.enatte {
  background-color: #e365 !important;
}
</style>