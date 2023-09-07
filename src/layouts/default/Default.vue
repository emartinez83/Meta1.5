<template>
  <v-app>

<v-navigation-drawer app>
  <DefaultSide app></DefaultSide>

</v-navigation-drawer>

   <v-main>
    <DefaultView></DefaultView>
  </v-main>
  
  </v-app>
</template>

<script setup>
  import DefaultBar from './AppBar.vue'
  import DefaultView from './View.vue'
  import DefaultSide from '@/components/Barra.vue'
</script>
