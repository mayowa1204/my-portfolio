<template>
  <v-app id="inspire">
    <v-navigation-drawer v-model="drawer" app permanent expand-on-hover>
      <v-list>
        <v-list-item class="px-2">
          <v-list-item-avatar>
            <v-img
              src="https://randomuser.me/api/portraits/women/85.jpg"
            ></v-img>
          </v-list-item-avatar>
        </v-list-item>

        <v-list-item link>
          <v-list-item-content>
            <v-list-item-title class="text-h6" style="color:#fff">
              Mayowa Oseni
            </v-list-item-title>
            <v-list-item-subtitle style="color:black"
              >oluwamayowaoseni12@gmail.com</v-list-item-subtitle
            >
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <v-divider></v-divider>

      <v-list dense nav>
        <v-list-item v-for="item in items" :key="item.title" :to="item.to" link>
          <v-list-item-icon>
            <v-icon style="color:#fff">{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title style="color:#fff">{{
              item.title
            }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
      <!--  -->
    </v-navigation-drawer>

    <v-main>
      <router-view></router-view>
    </v-main>
  </v-app>
</template>
<script>
export default {
  data: () => ({
    drawer: null,
    items: [
      { title: 'Dashboard', icon: 'mdi-view-dashboard', to: '/' },
      { title: 'About', icon: 'mdi-help-box', to: '/about' },
    ],
  }),
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #8b008b;
}

#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #8b008b;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
.v-navigation-drawer {
  background: #8b008b !important;
}
// .nav{

// }
</style>
