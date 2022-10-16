<template>
  <v-app>
    <v-app-bar app color="#C5E1A5" ldark  elevation="1"> 
      <v-app-bar-nav-icon @click.stop="sidebar = !sidebar"></v-app-bar-nav-icon>
      <v-spacer></v-spacer>
      <v-icon>mdi-mushroom</v-icon>      
      <v-icon>mdi-magnify </v-icon>       
    </v-app-bar>
    <v-navigation-drawer app v-model="sidebar"> 
      <v-list dense color="#C5E1A5">
        <v-list-item>
          <v-list-item-action>
            <v-icon @click.stop="sidebar = !sidebar">mdi-chevron-left-</v-icon>
          </v-list-item-action>
        </v-list-item>
      </v-list>
      <v-list-item>
        <v-list-item-content>Letícia Patricio</v-list-item-content>
      </v-list-item>
      <v-list>
        <v-list-item>
          <v-list-item-icon>
            <v-icon>
              mdi-heart
            </v-icon>
          </v-list-item-icon>
          <v-list-item-content>Favoritos</v-list-item-content>
        </v-list-item>
        <v-list-item>
          <v-list-item-icon>
            <v-icon>
              mdi-account-outline
            </v-icon>
          </v-list-item-icon>
          <v-list-item-content>Conta</v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-main>
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>

export default {
  data() {
    return {
      sidebar: false,
    }
  }
};
</script>
