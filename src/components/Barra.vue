<template>
  <v-card>
    <v-layout>
      <v-navigation-drawer app       
         v-model="drawer"
        :rail="rail"
        permanent
        @click="rail = false"
      
      >
        <v-list-item
          prepend-avatar="https://randomuser.me/api/portraits/men/85.jpg"
          title="Erick Martinez"
          nav
        >
          <template v-slot:append>
            <v-btn
              variant="text"
              icon="mdi-chevron-left"
              @click.stop="rail = !rail"
            ></v-btn>
          </template>
        </v-list-item>

        <v-divider></v-divider>

        <v-list density="compact" nav>
          <router-link to="/">
          <v-list-item prepend-icon="mdi-home" title="Home" value="home"></v-list-item>
          </router-link>
          <router-link to="/Imagen">
          <v-list-item prepend-icon="mdi-image" title="Imagen" value="imagen"></v-list-item>
        </router-link>
        <router-link to="/tabla">
          <v-list-item prepend-icon="mdi-table" title="Tabla" value="tabla"></v-list-item>
        </router-link>
        </v-list>
      </v-navigation-drawer>
      <v-main style="height: 200px"></v-main>
    </v-layout>
  </v-card>
</template>

<script>
  export default {
    data () {
      return {
        drawer: true,
        rail: true,
      }
    },
  }
</script>