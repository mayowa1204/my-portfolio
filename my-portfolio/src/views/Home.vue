<template>
  <div style=" background-image: linear-gradient(to right, #e6e6fa, white);">
    <section class="home  mx-auto" style="height:70vh; width:95%">
      <v-row
        class="mx-auto"
        justify="center"
        style="text-align:center; color:black"
      >
        <v-card
          class="mt-10 card"
          style="height:62vh; width:95%; background:	#FDF5E6; border-radius:200px"
        >
          <v-card-text style="height:100%">
            <v-row class="mx-auto" style="height:100%;" wrap no-gutters>
              <v-col cols="12" md="8">
                <div
                  style="margin-top:80px; width:60%; margin-left:120px"
                  class="hello-text"
                >
                  <h2
                    class="greeting"
                    style="font-size:30px; line-height: 1.2;text-align: justify;"
                  >
                    Hi, <br />
                    I'm Mayowa
                  </h2>
                  <p style="font-size:20px; text-align: justify;" class="mt-4">
                    I am an Engineer, and a full stack javascript developer. A
                    jack of all trades is a master of none but still much better
                    than a master of one.
                  </p>
                </div>
              </v-col>
              <v-col cols="12" md="4">
                <v-img
                  class="mt-4 picture"
                  height="400px"
                  width="400px"
                  style="border-radius:200px"
                  aspect-ratio="1"
                  src="../assets/photos/me/me.jpg"
                ></v-img>
              </v-col>
            </v-row>
          </v-card-text>
        </v-card>
      </v-row>
    </section>
    <section class="mx-auto home" style="height:70vh">
      <v-row
        class="mx-auto"
        justify="center"
        style="text-align:center; color:black"
      >
        <v-card
          class="mt-10 card"
          style="height:62vh; width:95%; background:	#FDF5E6;border-radius:20px"
        >
          <v-card-text style="height:100%">
            <v-row class="mx-auto" style="height:100%">
              <v-col cols="12" md="6" class="about">
                <h1 style="font-size:30px; margin-top:160px" class="about-me">
                  About Me
                </h1>
                <hr
                  style=" width: 20%;  height: 8px; background:	#C71585"
                  class=" mt-4 mx-auto"
                />
              </v-col>
              <v-col cols="12" md="6">
                <p
                  style="font-size:20px; margin-top:55px; text-align: justify;"
                >
                  Lorem ipsum dolor sit amet consectetur adipisicing elit.
                  Minima, eius provident atque quasi recusandae fugiat numquam
                  incidunt laudantium quia culpa error placeat nemo veritatis
                  officia aspernatur rerum praesentium voluptatibus aliquid?
                  Lorem ipsum dolor sit amet consectetur, adipisicing elit. Hic
                  sequi dignissimos ducimus numquam fugit perspiciatis,
                </p>

                <v-row style="width:100%" class="mt-6">
                  <v-col cols="6">
                    <v-btn style="background:	#C71585" rounded @click="goToAbout"
                      >Read more</v-btn
                    >
                  </v-col>
                  <v-col cols="6">
                    <a
                      download="CV.pdf"
                      class="pdf"
                      :href="require('../../public/assets/CV.pdf')"
                    >
                      <v-btn style="background:	#C71585" rounded
                        >Download CV
                      </v-btn>
                    </a>
                  </v-col>
                </v-row>
              </v-col>
            </v-row>
          </v-card-text>
        </v-card>
      </v-row>
    </section>
    <section class="mx-auto home" style="height:70vh;width:95%">
      <v-row
        class="mx-auto"
        justify="center"
        style="text-align:center; color:black"
      >
        <v-card
          class="mt-10 card"
          style="height:62vh; width:95%;  background:	#FDF5E6;border-radius:200px"
        >
          <v-card-text class="mt-6 mx-auto" style=" width:70%">
            <h2>Skills</h2>
            <p class="mt-3" style="font-size:16px">
              Lorem, ipsum dolor sit amet consectetur adipisicing elit.
              Necessitatibus deserunt repellendus perspiciatis veritatis.
            </p>
          </v-card-text>
          <v-card-text style="height:60%">
            <v-row class="mx-auto" style="height:100%">
              <v-carousel
                hide-delimiters
                style="height:100%; width:50%"
                class="mx-auto mt-n2"
              >
                <v-carousel-item v-for="(skill, i) in skills" :key="i">
                  <v-sheet height="100%" tile color="#FDF5E6">
                    <v-row
                      class="fill-height"
                      align="center"
                      style="width:100%;    height: 60%"
                      justify="center"
                    >
                      <v-img
                        contain
                        height="180px"
                        width="230px"
                        class="mx-auto"
                        aspect-ratio="1"
                        :src="skill.image"
                      />
                    </v-row>
                  </v-sheet>
                </v-carousel-item>
              </v-carousel>
            </v-row>
          </v-card-text>
        </v-card>
      </v-row>
    </section>
    <section class="footer" style="height:10vh"></section>
  </div>
</template>

<script>
// @ is an alias to /src
export default {
  name: 'Home',
  data: () => ({
    drawer: null,
    skills: [
      {
        name: 'HTML',
        image: require('../assets/photos/skills/html.png'),
      },
      { name: 'CSS', image: require('../assets/photos/skills/css.png') },
      {
        name: 'JavaScript',
        image: require('../assets/photos/skills/javascript.png'),
      },
      {
        name: 'TypeScript',
        image: require('../assets/photos/skills/typescript.png'),
      },
      {
        name: 'Node.js',
        image: require('../assets/photos/skills/node.js.png'),
      },
      {
        name: 'Nest.js',
        image: require('../assets/photos/skills/nest.js.png'),
      },
      { name: 'Vue.js', image: require('../assets/photos/skills/vue.js.jpg') },
      {
        name: 'PostgreSQL',

        image: require('../assets/photos/skills/postgreSQL.jpg'),
      },
      { name: 'MySQL', image: require('../assets/photos/skills/mysql.png') },
      {
        name: 'MongoDB',
        image: require('../assets/photos/skills/mongodb.jpg'),
      },
    ],
  }),
  methods: {
    goToAbout() {
      this.$router.push('/about')
    },
  },
}
</script>
<style scoped>
a,
a {
  text-decoration: none;
  color: black !important;
}
@media only screen and (min-device-width: 375px) and (max-device-width: 667px) and (-webkit-min-device-pixel-ratio: 2) {
  .home {
    height: 90vh !important;
  }
  .card {
    margin-top: 40px;
    height: 84vh !important;
  }
  .about {
    height: 10vh;
  }
  .about-me {
    font-size: 24px;
    margin-top: -2px !important;
    margin-top: 40px !important;
  }
  .greeting {
    margin-top: 70px;
  }
  .hello-text {
    width: 90% !important;
    margin-left: -10px !important;
    margin: auto !important;
  }
  .picture {
    margin-left: 80px !important;
    margin-top: -10px !important;
    height: 100px !important;
    width: 100px !important;
  }
}
@media only screen and (min-device-width: 414px) and (max-device-width: 736px) and (-webkit-min-device-pixel-ratio: 3) {
  .home {
    height: 90vh !important;
  }
  .card {
    margin-top: 40px;
    height: 84vh !important;
  }
  .about {
    height: 10vh;
  }
  .hello-text {
    width: 90% !important;
    margin-left: -10px !important;
    margin: auto !important;
  }
  .about-me {
    font-size: 24px;
    margin-top: -2px !important;
    margin-top: 40px !important;
  }

  .picture {
    margin-left: 50px !important;
    height: 200px !important;
    width: 200px !important;
  }
  .greeting {
    margin-top: 70px;
  }
}
@media only screen and (min-device-width: 375px) and (max-device-width: 812px) and (-webkit-min-device-pixel-ratio: 3) {
  .home {
    height: 90vh !important;
  }
  .card {
    margin-top: 40px;
    height: 84vh !important;
  }
  .greeting {
    margin-top: 70px;
  }
  .hello-text {
    width: 90% !important;
    margin-left: -10px !important;
    margin: auto !important;
  }
  .about {
    height: 10vh;
  }
  .about-me {
    font-size: 24px;
    margin-top: -2px !important;
    margin-top: 40px !important;
  }
  .picture {
    height: 200px !important;
    width: 200px !important;
  }
}
@media only screen and (min-device-width: 768px) and (max-device-width: 1024px) and (-webkit-min-device-pixel-ratio: 1) {
  .home {
    height: 90vh !important;
  }
  .card {
    margin-top: 40px;
    height: 84vh !important;
  }
  .about {
    height: 10vh;
  }
  .hello-text {
    width: 90% !important;
    margin-left: -10px !important;
    margin: auto !important;
  }
  .about-me {
    font-size: 24px;
    margin-top: -2px !important;
    margin-top: 40px !important;
  }
  .greeting {
    margin-top: 70px;
  }
  .picture {
    height: 200px !important;
    width: 200px !important;
  }
}

/* .home {
    background: url("../assets/piqsels.com-id-zwfiw.jpg") no-repeat center center fixed;
    background-size: cover;
  } */
</style>
