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
                    style="font-size:30px; line-height: 1.2;text-align: justify; color:#4B0082"
                  >
                    Hi, <br />
                    I'm Mayowa
                  </h2>
                  <p
                    style="font-size:20px; text-align: justify; color:#4B0082"
                    class="mt-4"
                  >
                    I am an Engineer, and a full stack javascript developer.
                  </p>
                  <h3
                    class="mt-3"
                    style=" line-height: 1.2;text-align: justify; color:#4B0082"
                  >
                    Favorite Quote:
                  </h3>
                  <p
                    style="font-size:20px; text-align: justify; color:#4B0082"
                    class="mt-2"
                  >
                    A jack of all trades is a master of none but still much
                    better than a master of one.
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
          style="height:62vh; width:95%; background:	#FDF5E6;border-radius:30px"
        >
          <v-card-text style="height:100%">
            <v-row class="mx-auto" style="height:100%">
              <v-col cols="12" md="6" class="about">
                <div
                  class="box-2 about-me"
                  style="font-size:24px; margin-top:140px"
                >
                  <div class="btn btn-two mx-auto">
                    <span class="mt-10 btn-text" style="color:#4B0082"
                      >About Me</span
                    >
                  </div>
                </div>
              </v-col>
              <v-col class="about-text" cols="12" md="6">
                <div style="width:95%; height:70%">
                  <p
                    style="font-size:20px; margin-top:55px; text-align: justify; line-height:1.5;color:#4B0082"
                  >
                    My full name is Oluwamayowa Titilopemi Oseni, I am a 22 year
                    old engineering graduate originally from Nigeria. I have a
                    BSc in Mechanical Engineering, and an MSc in Renewable
                    Energy Engineering, and I have recently worked as a software
                    delevloper at a tech startup.
                  </p>
                </div>

                <v-row style="width:50%; height:30%" class="buttons mx-auto">
                  <v-col cols="6" class="mx-auto">
                    <v-btn
                      style="background:#C71585; width:100%; text-transform:capitalize"
                      color="#4B0082"
                      rounded
                      @click="goToAbout"
                      >Read more</v-btn
                    >
                  </v-col>
                  <v-col cols="6" class="mx-auto">
                    <a
                      download="CV.pdf"
                      class="pdf"
                      :href="require('../../public/assets/CV.pdf')"
                    >
                      <v-btn
                        style="background:	#C71585; width:100%; text-transform:capitalize"
                        color="#4B0082"
                        rounded
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
          <v-card-text class="mt-6 mx-auto skills" style=" width:70%">
            <h2 style="color:#4B0082">Skills</h2>
            <p class="mt-3" style="font-size:16px;color:#4B0082">
              I have listed a few of my key web development skills. I have
              really enjoyed learning and growing in JavaScript and looking
              forward to mastering it. I am exited about exporing other
              programing languages and frameworks as well.
            </p>
          </v-card-text>
          <v-card-text style="height:60%">
            <v-row class="mx-auto" style="height:100%">
              <v-carousel
                hide-delimiters
                style="height:100%; width:50%"
                class="mx-auto mt-n2 slider"
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
.box-2 {
  background-color: #fdf5e6;
}
.btn {
  line-height: 50px;
  height: 150px;
  text-align: center;
  width: 350px;
  cursor: pointer;
}

.btn-two {
  color: black;
  transition: all 0.5s;
  position: relative;
}
.btn-two span {
  z-index: 2;
  display: block;
  position: absolute;
  width: 100%;
  height: 100%;
}
.btn-two::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
  transition: all 0.5s;
  border: 1px solid rgba(255, 255, 255, 0.2);
  background-color: rgba(255, 255, 255, 0.1);
}
.btn-two::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
  transition: all 0.5s;
  border: 1px solid #c71585;
  background-color: #fdf5e6;
}

span:hover {
  color: #fff;
}
.btn-two:hover::before {
  transform: rotate(-45deg);
  background-color: rgb(165, 131, 165);
}
.btn-two:hover::after {
  transform: rotate(45deg);
  background-color: #ddb9d7;
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
  .slider {
    width: 95% !important;
    height: 80% !important;
    margin-left: 15px !important;
    margin-top: 20px !important;
  }
  .skills {
    height: 35% !important;
    width: 92% !important;
  }
  .buttons {
    width: 100% !important;
    height: 15% !important;
  }
  .btn {
    line-height: 50px;
    height: 60px;
    text-align: center;
    width: 180px;
    cursor: pointer;
    margin: auto;
  }
  .btn-text {
    margin-top: 5px !important;
    font-size: 20px !important;
  }
  .picture {
    margin-left: 65px !important;
    margin-top: -20px !important;
    height: 120px !important;
    width: 120px !important;
  }
}
@media only screen and (min-device-width: 414px) and (max-device-width: 736px) and (-webkit-min-device-pixel-ratio: 3) {
  .home {
    height: 90vh !important;
  }
  .btn {
    line-height: 50px;
    height: 60px;
    text-align: center;
    width: 180px;
    cursor: pointer;
    margin: auto;
  }
  .btn-text {
    margin-top: 5px !important;
    font-size: 20px !important;
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
  .slider {
    width: 95% !important;
    height: 80% !important;
    margin-left: 15px !important;
    margin-top: 20px !important;
  }
  .skills {
    height: 35% !important;
    width: 92% !important;
  }

  .picture {
    margin-left: 50px !important;
    height: 200px !important;
    width: 200px !important;
  }
  .buttons {
    width: 95% !important;
    height: 15% !important;
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
  .btn {
    line-height: 50px;
    height: 60px;
    text-align: center;
    width: 180px;
    cursor: pointer;
    margin: auto;
  }
  .btn-text {
    margin-top: 5px !important;
    font-size: 20px !important;
  }
  .buttons {
    width: 95% !important;
    height: 15% !important;
  }
  .about-me {
    font-size: 24px;
    margin-top: -2px !important;
    margin-top: 60px !important;
  }
  .slider {
    width: 95% !important;
    height: 80% !important;
    margin-left: 15px !important;
    margin-top: 20px !important;
  }
  .skills {
    height: 35% !important;
    width: 92% !important;
  }
  .about-text {
    margin-top: -70px !important;
  }

  .picture {
    margin-left: 30px !important;
    margin-top: 30px !important;
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
  .btn {
    line-height: 50px;
    height: 60px;
    text-align: center;
    width: 180px;
    cursor: pointer;
    margin: auto;
  }
  .btn-text {
    margin-top: 5px !important;
    font-size: 20px !important;
  }
  .about-me {
    font-size: 24px;
    margin-top: -2px !important;
    margin-top: 60px !important;
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
