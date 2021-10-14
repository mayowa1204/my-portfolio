<template>
  <v-app id="inspire">
    <!-- <div class="nav" style=" height:8vh; width:90%; float:right; background:#E6E6FA">
      <div style=" width:25%; float:right">
        <v-row style=" width:40%; margin-left:150px">
          <v-col>
            <a
              target="_blank"
              href="https://www.linkedin.com/in/oluwamayowa-oseni-b04011172/"
            >
              <v-img
                height="20px"
                width="20px"
                class="mt-4"
                src="../assets/svgs/linkedin.svg"
              ></v-img>
            </a>
          </v-col>
          <v-col>
            <a target="_blank" href="https://twitter.com/Mayowa_titi">
              <v-img
                height="20px"
                width="20px"
                class="mt-4"
                src="../assets/svgs/twitter.svg"
              ></v-img>
            </a>
          </v-col>
          <v-col>
            <a target="_blank" href="https://instagram.com/mayowa_titi">
              <v-img
                height="20px"
                width="20px"
                class="mt-4"
                src="../assets/svgs/instagram.svg"
              ></v-img>
            </a>
          </v-col>
        </v-row>
      </div>
    </div> -->
    <v-navigation-drawer v-model="drawer" app permanent expand-on-hover>
      <v-list>
        <v-list-item class="px-2">
          <v-list-item-avatar>
            <v-img src="./assets/photos/me/myshot.jpg"></v-img>
          </v-list-item-avatar>
        </v-list-item>

        <v-list-item link>
          <v-list-item-content>
            <v-list-item-title class="text-h6" style="color:#fff">
              Mayowa Oseni
            </v-list-item-title>
            <v-list-item-subtitle style="color:black">
              <a href="/contact-me">
                oluwamayowaoseni12@gmail.com
              </a></v-list-item-subtitle
            >
            <v-list-item-subtitle>
              <div style=" width:100%">
                <v-row>
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
      { title: 'Home', icon: 'mdi-view-dashboard', to: '/' },
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
  // background: #8a2be2 #grad {
  background-image: linear-gradient(to right, #d8bfd8, #778899) !important;
  // background-image: url('./assets/africa2.jpg');
  // background-size: contain;
  // background-size: cover;
}
// .nav{

// }
</style>
