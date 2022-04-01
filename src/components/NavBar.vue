<template>
    <nav>
        <v-app-bar app color="pink darken-3" class="white--text">
            <v-app-bar-nav-icon class="pink darken-2 white--text" @click="drawer = !drawer"></v-app-bar-nav-icon>
            <v-toolbar-title tag="h2">
                <span class="font-weight-light">Hello</span>World
            </v-toolbar-title>
            <v-spacer></v-spacer> <!-- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -->
            <v-menu>
                <template v-slot:activator="{ on, attrs }">
                    <v-btn plain class="mr-5" color="white--text" dark v-bind="attrs" v-on="on">
                        <v-icon left>mdi-dialpad</v-icon>
                        Menu
                    </v-btn>
                </template>
                <v-list>
                    <v-list-item v-for="item in navItems" :key="item.id" router :to="item.route">
                        <v-list-item-icon>
                            <v-icon class="pink--text" right>mdi-{{ item.icon }}</v-icon>
                        </v-list-item-icon>
                        <v-list-item-title>{{ item.text }}</v-list-item-title>
                    </v-list-item>
                </v-list>
            </v-menu>
            <v-btn>
                <span>Sign out</span>
                <v-icon right>mdi-exit-to-app</v-icon>
            </v-btn>
        </v-app-bar>
         <!-- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -->
        <v-navigation-drawer v-model="drawer" app class="pink darken-3">
            <v-layout column align-center>
                <v-flex class="mt-7">
                    <v-avatar size="100">
                        <v-img src="https://i.pinimg.com/originals/68/16/3e/68163efb3c2201721d8e681cde6aef2b.jpg"></v-img>
                    </v-avatar>
                </v-flex>
                <p class="white--text mt-2">Mohamed Semlali</p>
            </v-layout>
            <v-list>
                <v-list-item v-for="item in navItems" :key="item.id" class="white--text" router :to="item.route">
                    <v-list-item-icon>
                        <v-icon class="white--text" right>mdi-{{ item.icon }}</v-icon>
                    </v-list-item-icon>
                    <v-list-item-title>
                        {{ item.text }}
                    </v-list-item-title>
                </v-list-item>
            </v-list>
        </v-navigation-drawer>
    </nav>
</template>

<script>

export default {
    data() {
        return {
            drawer: false,
            navItems: [
                {id: 1, icon: "view-dashboard", text:"Dashboard", route: "/"},
                {id: 2, icon: "folder", text:"My Project", route: "/projects"},
                {id: 3, icon: "information", text:"About", route: "/about"},
            ]
        }
  }
}
</script>