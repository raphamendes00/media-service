<template>
  <v-app>

    <v-layout>

      <v-app-bar class="app-bar" color="primary">
        <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
        <v-toolbar-title>Media Service</v-toolbar-title>
      </v-app-bar>
  
      <v-navigation-drawer v-model="drawer">
        <div class="mt-5">
          <v-list-item link prepend-icon="mdi-image-multiple-outline" title="Exibir imagens" ></v-list-item>
          <v-list-item link prepend-icon="mdi-book-cross" title="Bíblia" ></v-list-item>
          <v-list-item link prepend-icon="mdi-bullhorn-outline" title="Avisos" ></v-list-item>
        </div>
      </v-navigation-drawer>

      <v-main>
        <router-view />
      </v-main>

    </v-layout>

  </v-app>
</template>

<script lang="ts" setup>
import { ref } from "vue";

const drawer = ref(false);
</script>

<style>
  .app-bar {
    border-radius: 0px 0px 10px 10px;
  }
</style>