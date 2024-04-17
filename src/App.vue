<template>
  <v-app>
    <v-toolbar density="compact">
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>
        <router-link to="/">Vuetify</router-link>
      </v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon @click="toggleTheme">
        <v-icon>mdi-theme-light-dark</v-icon>
      </v-btn>

      <v-btn icon>
        <!-- <v-icon>mdi-dots-vertical</v-icon> -->
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>

      <v-btn
        to="/login"
        variant="outlined"
        color="blue-accent-3"
        size="small"
        text="login"
      >
      </v-btn>
    </v-toolbar>
    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script setup>
import { useTheme } from "vuetify";

const theme = useTheme();

function toggleTheme() {
  console.log(theme.global.current.value.dark);
  theme.global.name.value = theme.global.current.value.dark ? "light" : "dark";
}
</script>
