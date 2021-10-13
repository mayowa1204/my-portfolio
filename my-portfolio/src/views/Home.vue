<template>
  <div style=" background:	#E6E6FA">
    <div class="nav" style=" height:10vh; width:100%">
      <div style=" width:25%; float:right">
        <v-row style=" width:40%; margin-left:100px">
          <v-col>
            <a href="https://www.linkedin.com/in/oluwamayowa-oseni-b04011172/">
              <v-img
                height="20px"
                width="20px"
                class="mt-4"
                src="../assets/svgs/linkedin.svg"
              ></v-img>
            </a>
          </v-col>
          <v-col>
            <a href="https://twitter.com/Mayowa_titi">
              <v-img
                height="20px"
                width="20px"
                class="mt-4"
                src="../assets/svgs/twitter.svg"
              ></v-img>
            </a>
          </v-col>
          <v-col>
            <a href="https://instagram.com/mayowa_titi">
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
    </div>
    <section class="home" style="height:70vh; width:100%">
      <v-row
        class="mx-auto"
        justify="center"
        style="text-align:center; color:black"
      >
        <v-card class="mt-2" style="height:62vh; width:95%; background:	#98FB98">
          <v-card-text style="height:100%">
            <v-row class="mx-auto" style="height:100%">
              <v-col cols="8">
                <div style="margin-top:80px; width:60%; margin-left:120px">
                  <h2
                    style="font-size:30px; line-height: 1.2;text-align: justify;"
                  >
                    Hi, <br />
                    I'm Mayowa
                  </h2>
                  <p style="font-size:20px; text-align: justify;" class="mt-4">
                    Lorem ipsum dolor, sit amet consectetur adipisicing elit.
                    Dicta officia neque aperiam iste, deserunt enim quibusdam
                    nemo quisquam laboriosam perspiciatis est. Sunt culpa
                    pariatur dolores consequuntur nam, commodi distinctio
                    minima.
                  </p>
                </div>
              </v-col>
              <v-col cols="4">
                <v-img
                  height="400px"
                  width="400px"
                  style="border-radius:200px"
                  aspect-ratio="1"
                  src="../assets/me-main.jpg"
                ></v-img>
              </v-col>
            </v-row>
          </v-card-text>
        </v-card>
      </v-row>
    </section>
    <section style="height:70vh">
      <v-row
        class="mx-auto"
        justify="center"
        style="text-align:center; color:black"
      >
        <v-card class="mt-2" style="height:62vh; width:95%; background:	#98FB98">
          <v-card-text style="height:100%">
            <v-row class="mx-auto" style="height:100%">
              <v-col cols="6">
                <h1 style="font-size:30px; margin-top:160px">About Me</h1>
                <hr
                  style=" width: 20%;  height: 8px; background:#8A2BE2"
                  class=" mt-4 mx-auto"
                />
              </v-col>
              <v-col cols="6">
                <p
                  style="font-size:20px; margin-top:100px; text-align: justify;"
                >
                  Lorem ipsum dolor sit amet consectetur adipisicing elit.
                  Minima, eius provident atque quasi recusandae fugiat numquam
                  incidunt laudantium quia culpa error placeat nemo veritatis
                  officia aspernatur rerum praesentium voluptatibus aliquid?
                  Lorem ipsum dolor sit amet consectetur, adipisicing elit. Hic
                  sequi dignissimos ducimus numquam fugit perspiciatis, expedita
                  nam magni ipsum debitis odio, est aliquam modi culpa, sint
                  iure repudiandae deleniti maiores!lorem Lorem ipsum dolor sit
                  amet, consectetur adipisicing elit. Maiores quo, error
                  possimus recusandae accusantium ad cum veritatis. Ut, quis!
                  Exercitationem, facilis rem cupiditate eligendi assumenda
                  architecto dolore repellat aliquam animi.
                </p>

                <v-row style="width:100%" class="mt-6">
                  <v-col cols="6">
                    <v-btn @click="goToAbout">Read more</v-btn>
                  </v-col>
                  <v-col cols="6">
                    <a
                      download="CV.pdf"
                      :href="require('../../public/assets/CV.pdf')"
                      ><v-btn>Download CV </v-btn></a
                    >
                  </v-col>
                </v-row>
              </v-col>
            </v-row>
          </v-card-text>
        </v-card>
      </v-row>
    </section>
    <section style="height:70vh">
      <v-row
        class="mx-auto"
        justify="center"
        style="text-align:center; color:black"
      >
        <v-card
          class="mt-2"
          style="height:62vh; width:95%;  background:	#98FB98"
        >
          <v-card-text class="mt-6 mx-auto" style=" width:70%">
            <h2>Skills</h2>
            <p class="mt-3">
              Lorem, ipsum dolor sit amet consectetur adipisicing elit.
              Necessitatibus deserunt repellendus perspiciatis veritatis.
              Sapiente neque, rem aliquid qui aperiam magni autem provident,
              dolore nobis minus maxime consequatur. Quisquam, quidem magnam!
            </p>
          </v-card-text>
          <v-card-text style="height:70%">
            <v-row class="mx-auto" style="height:100%">
              <v-carousel
                hide-delimiters
                style="height:100%; width:50%"
                class="mx-auto mt-n2"
              >
                <v-carousel-item v-for="(skill, i) in skills" :key="i">
                  <v-sheet height="100%" tile>
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
        image: require('../assets/html.png'),
      },
      { name: 'CSS', image: require('../assets/css.png') },
      {
        name: 'JavaScript',
        image: require('../assets/javascript.png'),
      },
      {
        name: 'TypeScript',
        image: require('../assets/typescript.png'),
      },
      { name: 'Node.js', image: require('../assets/node.js.png') },
      { name: 'Nest.js', image: require('../assets/nest.png') },
      { name: 'Vue.js', image: require('../assets/logo.png') },
      {
        name: 'PostgreSQL',

        image: require('../assets/postgreSQL.jpg'),
      },
      { name: 'MySQL', image: require('../assets/mysql.png') },
      { name: 'MongoDB', image: require('../assets/mongodb.jpg') },
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
a:hover {
  background-color: transparent;
}
/* .home {
    background: url("../assets/piqsels.com-id-zwfiw.jpg") no-repeat center center fixed;
    background-size: cover;
  } */
</style>
