<template>
  <div style=" background-image: linear-gradient(to right, #e6e6fa, white);">
    <section class="mx-auto" style="height:70vh">
      <v-row class="mx-auto" style="height:100%">
        <v-card
          style="width:90%; height:90%; background:#FDF5E6;"
          elevation="0"
          class="mx-auto mt-10"
        >
          <v-card-text>
            <v-row style="height:90%" wrap no-gutters>
              <v-col cols="12" md="6" class="image">
                <v-row class="mx-auto mt-10 " style="height:90%; width:100%">
                  <v-carousel
                    hide-delimiters
                    style="height:90%; width:100%;"
                    class="mx-auto mt-n2"
                  >
                    <v-carousel-item v-for="(image, i) in me" :key="i">
                      <v-sheet height="70%" tile color="#FDF5E6">
                        <v-row
                          class="fill-height"
                          align="center"
                          style="width:100%;    height: 60%"
                          justify="center"
                        >
                          <v-img
                            contain
                            height="400px"
                            width="400px"
                            class="picture mx-auto mt-3"
                            aspect-ratio="1"
                            :src="image.image"
                          />
                        </v-row>
                      </v-sheet>
                    </v-carousel-item>
                  </v-carousel>
                </v-row>
              </v-col>
              <v-col cols="12" md="6" class="text" style="height:100%">
                <div class="mx-auto" style="width:90%">
                  <h2 class="mt-5" style="text-align:center">More About Me</h2>
                  <p class="mt-5" style="text-align:justify">
                    Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                    Odio natus numquam quia eaque voluptate cumque? Tempore
                    debitis voluptates saepe facilis ea eum! Blanditiis dolorum
                    ipsum recusandae rem. Quae, eius asperiores.
                  </p>
                </div>
              </v-col>
            </v-row>
          </v-card-text>
        </v-card>
      </v-row>
    </section>
    <section class="mx-auto" style="height:70vh">
      <v-row class="mx-auto" style="height:100%">
        <v-card
          style="width:90%; height:90%; background:#FDF5E6;"
          elevation="0"
          class="mx-auto mt-10"
        >
          <v-card-text>
            <v-row style="height:90%">
              <v-col cols="12" md="6" class="education">
                <v-img
                  class="picture mx-auto mt-10"
                  height="400px"
                  width="400px"
                  aspect-ratio="1"
                  src="../assets/photos/education/grad.png"
                >
                </v-img>
              </v-col>
              <v-col cols="12" md="6" class="text">
                <div class="mx-auto" style="width:90%">
                  <h2 class="mt-5" style="text-align:center">Education</h2>
                  <p class="mt-5" style="text-align:justify">
                    Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                    Nemo nisi vel laborum quisquam, repellat ab reprehenderit ea
                    excepturi expedita? Autem numquam perferendis dicta veniam
                    sint, quod aspernatur reiciendis ex rem?
                  </p>
                </div></v-col
              >
            </v-row>
          </v-card-text>
        </v-card>
      </v-row>
    </section>
    <section style="height:70vh;">
      <v-row class="mx-auto" style="height:100%">
        <v-card
          style="width:90%; height:90%; background:#FDF5E6;"
          elevation="0"
          class="mx-auto mt-10"
        >
          <v-card-text>
            <v-row style="height:90%">
              <v-col cols="12" md="6" class=" image">
                <v-row class="mx-auto mt-10 " style="height:90%; width:100%">
                  <v-carousel
                    hide-delimiters
                    style="height:90%; width:100%;"
                    class="mx-auto mt-n2"
                  >
                    <v-carousel-item v-for="(hobby, i) in hobbies" :key="i">
                      <v-sheet height="70%" tile color="#FDF5E6">
                        <v-row
                          class="fill-height"
                          align="center"
                          style="width:100%;    height: 60%"
                          justify="center"
                        >
                          <v-img
                            contain
                            height="400px"
                            width="400px"
                            class="picture mx-auto"
                            aspect-ratio="1"
                            :src="hobby.image"
                          />
                        </v-row>
                      </v-sheet>
                    </v-carousel-item>
                  </v-carousel>
                </v-row>
              </v-col>
              <v-col cols="12" md="6" class="text">
                <div class="mx-auto" style="width:90%">
                  <h2 class="mt-5" style="text-align:center">Hobbies</h2>
                  <p class="mt-5" style="text-align:jsutify">
                    Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                    Cum nemo asperiores non ipsa doloremque praesentium expedita
                    unde consectetur nam! Consequuntur facilis quae quibusdam
                    molestiae rem accusantium qui nostrum quis exercitationem!
                  </p>
                </div>
              </v-col>
            </v-row>
          </v-card-text>
        </v-card>
      </v-row>
    </section>
    <section class="mx-auto" style="height:70vh">
      <v-row class="mx-auto" style="height:100%">
        <v-card
          style="width:90%; height:90%; background:#FDF5E6;"
          elevation="0"
          class="mx-auto mt-10"
        >
          <v-card-text>
            <v-row style="height:90%">
              <v-col cols="12" md="6" class=" image">
                <v-row class="mx-auto mt-10 " style="height:90%; width:100%">
                  <v-carousel
                    hide-delimiters
                    style="height:90%; width:100%;"
                    class="mx-auto mt-n2"
                  >
                    <v-carousel-item v-for="(travel, i) in travels" :key="i">
                      <v-sheet height="70%" tile color="#FDF5E6">
                        <v-row
                          class="fill-height"
                          align="center"
                          style="width:100%;    height: 60%"
                          justify="center"
                        >
                          <v-img
                            contain
                            height="400px"
                            width="400px"
                            class="picture mx-auto"
                            aspect-ratio="1"
                            :src="travel.image"
                          />
                        </v-row>
                      </v-sheet>
                    </v-carousel-item>
                  </v-carousel>
                </v-row>
              </v-col>
              <v-col cols="12" md="6" class="text">
                <div class="mx-auto" style="width:90%">
                  <h2 class="mt-5" style="text-align:center">Travel</h2>
                  <p class="mt-5" style="text-align:justify">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Debitis quibusdam perferendis illum distinctio, qui fugit
                    alias sint maiores nobis deserunt impedit eligendi
                    consectetur soluta asperiores doloribus voluptatibus error
                    voluptate mollitia.
                  </p>
                </div></v-col
              >
            </v-row>
          </v-card-text>
        </v-card>
      </v-row>
    </section>
    <section class="footer" style=" height:10vh"></section>
  </div>
</template>
<script>
export default {
  name: 'About',
  data: () => ({
    me: [
      { image: require('../assets/photos/me/myshot.jpg') },
      {
        image: require('../assets/photos/me/me.jpg'),
      },
      {
        image: require('../assets/photos/me/pageant.jpg'),
      },
    ],
    hobbies: [
      {
        image: require('../assets/photos/hobbies/climbing.jpg'),
      },
      { image: require('../assets/photos/hobbies/cnc.jpg') },
      {
        image: require('../assets/photos/hobbies/funeral.jpg'),
      },
      {
        image: require('../assets/photos/hobbies/music.jpg'),
      },
      {
        image: require('../assets/photos/hobbies/singing.jpg'),
      },
    ],
    travels: [
      { image: require('../assets/photos/travel/monkey.jpg') },
      {
        image: require('../assets/photos/travel/colage.jpg'),
      },
      {
        image: require('../assets/photos/travel/park.jpg'),
      },
    ],
  }),
}
</script>
<style>
/* Portrait and Landscape */
@media only screen and (min-device-width: 375px) and (max-device-width: 667px) and (-webkit-min-device-pixel-ratio: 2) {
  .image {
    height: 30vh;
    margin-top: -50px;
  }
  .education {
    height: 30%;
  }
  .text {
    margin-top: -30px !important;
  }

  .picture {
    height: 100px !important;
    width: 100px !important;
  }
}
@media only screen and (min-device-width: 414px) and (max-device-width: 736px) and (-webkit-min-device-pixel-ratio: 3) {
  .image {
    height: 30vh;
    margin-top: -50px;
  }
  .education {
    height: 30%;
  }
  .text {
    margin-top: -30px !important;
  }
  .picture {
    height: 100px !important;
    width: 100px !important;
  }
}
@media only screen and (min-device-width: 375px) and (max-device-width: 812px) and (-webkit-min-device-pixel-ratio: 3) {
  .image {
    height: 30vh;
    margin-top: -50px;
  }
  .education {
    height: 30%;
  }
  .text {
    margin-top: -30px !important;
  }
  .picture {
    height: 100px !important;
    width: 100px !important;
  }
}
@media only screen and (min-device-width: 768px) and (max-device-width: 1024px) and (-webkit-min-device-pixel-ratio: 1) {
  .image {
    height: 35vh;
    margin-top: -50px;
  }
  .education {
    height: 30%;
  }
  .text {
    margin-top: -30px !important;
  }
  .picture {
    height: 200px !important;
    width: 200px !important;
  }
}
</style>
