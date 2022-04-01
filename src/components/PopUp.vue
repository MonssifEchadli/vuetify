<template>
    <v-dialog max-width="600px">
        <template v-slot:activator="{ on, attrs }">
            <v-btn text class="white darken-3 pink--text mr-3" v-bind="attrs" v-on="on">
                Add new project
                <v-icon right>mdi-plus</v-icon>
            </v-btn>
        </template>
        <v-card>
            <v-card-title>
                <h5>ADD NEW PROJECT</h5>
            </v-card-title>
            <v-card-text>
                <v-form ref="form" v-model="valid" lazy-validation>
                    <v-text-field prepend-icon="mdi-dialpad" v-model="project.titre" :counter="30" label="Title" required></v-text-field>
                    <v-textarea prepend-icon="mdi-message-text" v-model="project.text" :counter="500" label="text" required></v-textarea>
                    <v-select prepend-icon="mdi-call-split" v-model="project.etat" :items="allEtat" label="Etat" required></v-select>
                    
                    <v-btn :disabled="!valid" color="success darken-3" class="mr-4" @click="validate">ADD</v-btn>
                    <v-btn color="pink darken-3" dark @click="reset">RESET</v-btn>
                </v-form>
            </v-card-text>
        </v-card>
    </v-dialog>
</template>

<script>
export default({
    data() {
       return {
           valid: true,
           project: {
                etat: '', 
                titre: '', 
                text: '',
           },
           allEtat: ['termin', 'encour', 'enatte'],
       } 
    },
    methods: {
        validate () {
            console.log(this.project)
            this.$refs.form.validate()
        },
        reset() {
            this.$refs.form.reset()
        }
    }
})
</script>
