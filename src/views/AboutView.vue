<template>
  <div class="about margin10">
    <h1 class="subtitle-1 grey--text">About Us</h1>
    <v-container class="my-5">
      <v-layout row>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Minima soluta in iste repudiandae atque quisquam distinctio, commodi iusto, mollitia, aliquid ipsa consequatur quasi natus quaerat expedita molestiae! Unde, minus deleniti.
        Distinctio quasi ratione reiciendis incidunt, accusantium similique soluta blanditiis labore vero ipsam maiores voluptate tempore a sed sint dolorem, ab ad delectus!
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Voluptates ratione iusto inventore error dolorem odio neque unde dignissimos totam eius recusandae nihil, soluta iste praesentium, delectus, quasi dolore. Accusantium, fugit?
      </v-layout>
    </v-container>
    <h1 class="subtitle-1 grey--text">Our skills</h1>
    <v-container class="my-5">
      <v-layout row class="mb-5">
        <v-flex xs12 md6 lg4 v-for="s in skills" :key="s.id">
          <v-card flat class="ma-3 pa-3">
            <v-responsive>
              <!--
              <v-card flat class=" text-center mt-3">
                <v-avatar size="100">
                  <v-img :src="s.img"></v-img>
                </v-avatar>
              </v-card>
              -->
              <v-img max-height="150" :src="s.img"></v-img>
            </v-responsive>
            <v-card-title>
              {{ s.nom }}
            </v-card-title>
            <v-card-subtitle>
              {{ s.text }}
            </v-card-subtitle>
            <v-card-text>
              Niveau : 
              <span class="skillsColor" v-for="i in s.niveau" :key="i"> &block;</span>
              <span style="float: right;">{{ s.niveau }}/10</span>
            </v-card-text>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<script>

export default {
  data() {
    return {
      skills: [
        {id: 1, niveau: 8, nom: "JEE", text: "Distinctio quasi ratione reiciendis, accusantium!", img: "https://picsum.photos/id/1/500/300"},
        {id: 2, niveau: 7, nom: "JAVA", text: "Distinctd quasi ratione reiciendis, accusantium!", img: "https://picsum.photos/id/6/500/300"},
        {id: 3, niveau: 3, nom: "JEE", text: "Distinctio quasi ratione reiciendis, accusantium!", img: "https://picsum.photos/id/3/500/300"},
        {id: 4, niveau: 6, nom: "JAVA", text: "Distinctx quasi ratione reiciendis, accusantium!", img: "https://picsum.photos/id/8/500/300"},
      ],
    }
  },
  methods: {
    
  }
}

</script>

<style scoped>
.skillsColor {
  color: #bb4477;
}
</style>