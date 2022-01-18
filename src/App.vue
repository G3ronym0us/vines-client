<template>
  <v-app>
    <v-navigation-drawer color="grey lighten-4" app>
      <br>
      <v-img 
        src="@/assets/logo.png"
      ></v-img>
      <hr>
      <v-list
        dense
        nav
      >
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
        >
          <v-list-item-icon>
            <v-icon color="#e6af41">{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content class="titulo">
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app>
      <!-- -->
    </v-app-bar>

    <!-- Sizes your content based upon application components -->
    <v-main>

      <!-- Provides the application the proper gutter -->
      <v-container fluid>

        <!-- If using vue-router -->
        <router-view></router-view>
      </v-container>
    </v-main>

    <v-footer app>
      <!-- -->
    </v-footer>
  </v-app>
</template>

<script>
  export default {
    data () {
      return {
        drawer: true,
        items: [
          { title: 'Comprar GoldUSD', icon: 'mdi-circle-multiple' },
          { title: 'Vender GoldUSD', icon: 'mdi-circle-multiple' },
          { title: 'Transferir', icon: 'mdi-circle-multiple' },
          { title: 'Saldo GoldUSD', icon: 'mdi-wallet' },
          { title: 'Operaciones', icon: 'mdi-swap-horizontal' },
          { title: 'Mis Operaciones', icon: 'mdi-swap-horizontal' },
          { title: 'Historial', icon: 'mdi-history' }
        ],
        rigth: true
      }
    },
  }
</script>

<style>
  body{
    height: 100vh;
  }

  .v-card{
    height: 100vh;
  }

  hr{
    width: 90%;
    margin: auto;
    margin-top: 20px;
    margin-bottom: 20px;
  }

  .titulo{
    background-color: #5A2980;
    color: #FFFFFF;
    border-radius: 5px;
    margin-left: -20px;
  }

</style>