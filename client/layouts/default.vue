<template>
  <div>
    <v-app style="font-family: 'Prompt', sans-serif;">

      <div>
        <v-app-bar
            color="deep-purple accent-4"
            dense
            dark
        >

          <AppBar/>

          <v-toolbar-title>Mango</v-toolbar-title>

          <v-spacer></v-spacer>

          <v-btn icon>
            <v-icon>mdi-heart</v-icon>
          </v-btn>

          <v-menu
              left
              bottom
          >
            <template v-slot:activator="{ on, attrs }">
              <v-btn
                  icon
                  v-bind="attrs"
                  v-on="on"
              >
                <v-icon>mdi-dots-vertical</v-icon>
              </v-btn>
            </template>

            <v-list>
              <v-list-item
                  v-for="n in 5"
                  :key="n"
                  @click="() => {}"
              >
                <v-list-item-title>Option {{ n }}</v-list-item-title>
              </v-list-item>
            </v-list>
          </v-menu>
        </v-app-bar>
      </div>

      <v-container justify="center" align="center">
        <Nuxt/>
      </v-container>

    </v-app>
  </div>
</template>

<script>
import AppBar from "../components/layout/AppBar";
export default {
  components: {AppBar},
  data() {
    return {
    }
  }
}
</script>

<style scoped>
</style>