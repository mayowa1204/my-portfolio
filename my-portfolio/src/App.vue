<template>
  <v-app id="inspire">
    <v-navigation-drawer v-model="drawer" app permanent expand-on-hover>
      <v-list>
        <v-list-item class="px-2">
          <v-list-item-avatar>
            <v-img src="./assets/photos/me/myshot.jpg"></v-img>
          </v-list-item-avatar>
        </v-list-item>

        <v-list-item link>
          <v-list-item-content>
            <v-list-item-title class="text-h6" style="color:black">
              Mayowa Oseni
            </v-list-item-title>
            <v-list-item-subtitle>
              <a @click="goToContactMe" style="color:black">
                oluwamayowaoseni12@gmail.com
              </a></v-list-item-subtitle
            >
            <v-list-item-subtitle>
              <div style=" width:100%">
                <v-row>
                  <v-col>
                    <a target="_blank" href="https://github.com/mayowa1204">
                      <v-img
                        height="20px"
                        width="20px"
                        class="mt-4"
                        src="./assets/svgs/github.svg"
                      ></v-img>
                    </a>
                  </v-col>
                  <v-col>
                    <a
                      target="_blank"
                      href="https://www.linkedin.com/in/oluwamayowa-oseni-b04011172/"
                    >
                      <v-img
                        height="20px"
                        width="20px"
                        class="mt-4"
                        src="./assets/svgs/linkedin.svg"
                      ></v-img>
                    </a>
                  </v-col>
                  <v-col>
                    <a target="_blank" href="https://twitter.com/Mayowa_titi">
                      <v-img
                        height="20px"
                        width="20px"
                        class="mt-4"
                        src="./assets/svgs/twitter.svg"
                      ></v-img>
                    </a>
                  </v-col>
                  <v-col>
                    <a target="_blank" href="https://instagram.com/mayowa_titi">
                      <v-img
                        height="20px"
                        width="20px"
                        class="mt-4"
                        src="./assets/svgs/instagram.svg"
                      ></v-img>
                    </a>
                  </v-col>
                </v-row>
              </div>
            </v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <v-divider></v-divider>

      <v-list dense nav>
        <v-list-item v-for="item in items" :key="item.title" :to="item.to" link>
          <v-list-item-icon>
            <v-icon style="color:black">{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title style="color:black">{{
              item.title
            }}</v-list-item-title>
          </v-list-item-content>
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
  data: () => ({
    drawer: null,
    items: [
      { title: 'Home', icon: 'mdi-view-dashboard', to: '/' },
      { title: 'About', icon: 'mdi-help-box', to: '/about' },
    ],
  }),
  methods: {
    goToContactMe() {
      this.$router.push('/contact-me')
    },
  },
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

#nav {
  padding: 30px;
  a {
    font-weight: bold;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
.v-navigation-drawer {
  background-image: linear-gradient(to right, #d8bfd8, #778899) !important;
}
</style>
