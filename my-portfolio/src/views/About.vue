<template>
  <div style=" background-image: linear-gradient(to right, #e6e6fa, white);">
    <section class="mx-auto card" style="height:70vh">
      <v-row class="mx-auto" style="height:100%">
        <v-card
          style="width:90%; height:90%; background:#FDF5E6; border-radius:30px"
          elevation="0"
          class="mx-auto mt-10"
        >
          <v-card-text>
            <v-row style="height:90%" wrap no-gutters>
              <v-col cols="12" md="6" class="image mx-auto">
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
                <div class="mx-auto" style="width:90%;text-align:center">
                  <h2
                    class="heading mt-5 underline-to-top"
                    style="text-align:center; color:#4B0082"
                  >
                    More About Me
                  </h2>
                  <p
                    class="paragraph mt-10"
                    style="text-align:justify; font-size:20px; line-height:1.8; color:#4B0082"
                  >
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
    <section class="mx-auto card" style="height:70vh">
      <v-row class="mx-auto " style="height:100%">
        <v-card
          style="width:90%; height:90%; background:#FDF5E6; border-radius:30px"
          elevation="0"
          class="mx-auto mt-10 card"
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
                <div class="mx-auto" style="width:90%; text-align:center">
                  <h2
                    class="heading education mt-5 underline-to-top"
                    style="text-align:center; color:#4B0082"
                  >
                    Education
                  </h2>
                  <h3 class="mt-7" style="text-align:justify; color:#4B0082">
                    Masters:
                  </h3>
                  <p
                    class="paragraph2"
                    style="font-size:16px; text-align:justify; color:#4B0082"
                  >
                    MSc. Renewable Energy Engineering. <br />
                    University of Exeter
                  </p>
                  <h3 style="text-align:justify; color:#4B0082">
                    Bachelors:
                  </h3>
                  <p
                    class="paragraph2"
                    style="font-size:16px; text-align:justify; color:#4B0082"
                  >
                    BSc. Mechanical Engineering. <br />
                    University of Mines and Technology
                  </p>
                  <h3 style="text-align:justify; color:#4B0082">
                    Key Modules:
                  </h3>
                  <p
                    class="paragraph2"
                    style="text-align:justify; font-size:16px; line-height:1.5; color:#4B0082"
                  >
                    Wind Energy Technology,Renewable heating, as well as
                    Hydropower, Geothermal Energy. Themes in Climate Change,
                    Sustainable Architecture, Solar Research and Low Carbon
                    Vehicles. Materials design, Thermodynamics, Hydraulic
                    machinery, Fluid Mechanics Machine Design, Ethics in
                    Science, Business Entrepreneurship, Computer Aided Design
                    (AutoCad, Solidworks)
                  </p>
                </div></v-col
              >
            </v-row>
          </v-card-text>
        </v-card>
      </v-row>
    </section>
    <section style="height:70vh;" class="card">
      <v-row class="mx-auto hobbies" style="height:100%">
        <v-card
          style="width:90%; height:90%; background:#FDF5E6; border-radius:30px"
          elevation="0"
          class="mx-auto mt-10"
        >
          <v-card-text>
            <v-row style="height:90%">
              <v-col cols="12" md="6" class="image mx-auto">
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
                <div class="mx-auto " style="width:90%;text-align:center">
                  <h2
                    class="heading mt-5 underline-to-top"
                    style="text-align:center; color:#4B0082"
                  >
                    Hobbies
                  </h2>
                  <p
                    class="paragraph mt-10"
                    style=" font-size:20px; line-height:1.8;text-align:justify; color:#4B0082"
                  >
                    I am not a typical girly girl, I love out door activities
                    like hiking and climbing, completing obstacle courses,
                    visting wild life reserves and traveling which i'll dive
                    deep into in the next section. My second love is music. I
                    wish i would study music some time later in life, i am
                    fascinated with the art and the amount of hard work and
                    dedication it takes to produce a good piece
                  </p>
                </div>
              </v-col>
            </v-row>
          </v-card-text>
        </v-card>
      </v-row>
    </section>
    <section class="mx-auto card" style="height:70vh">
      <v-row class="mx-auto" style="height:100%">
        <v-card
          style="width:90%; height:90%; background:#FDF5E6; border-radius:30px"
          elevation="0"
          class="mx-auto mt-10"
        >
          <v-card-text>
            <v-row style="height:90%">
              <v-col cols="12" md="6" class="image mx-auto">
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
                <div class="mx-auto" style="width:90%; text-align:center">
                  <h2
                    class="heading mt-5 underline-to-top"
                    style="text-align:center; color:#4B0082"
                  >
                    Travel
                  </h2>
                  <p
                    class="paragraph mt-10"
                    style="text-align:justify; font-size:20px; line-height:1.8; color:#4B0082"
                  >
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
.underline-to-top {
  background-image: linear-gradient(120deg, #84fab0 0%, #8fd3f4 100%);
  background-repeat: no-repeat;
  background-size: 100% 0.2em;
  background-position: 0 88%;
  transition: background-size 0.25s ease-in;
}
.underline-to-top:hover {
  background-size: 100% 88%;
}
.heading {
  color: black;
  text-transform: capitalize;
  text-decoration: none;
  letter-spacing: 0.15em;

  display: inline-block;
  padding: 15px 20px;
  position: relative;
}
.heading:after {
  background: none repeat scroll 0 0 transparent;
  bottom: 0;
  content: '';
  display: block;
  height: 2px;
  left: 50%;
  position: absolute;
  background: rgb(220, 95, 192);
  transition: width 0.3s ease 0s, left 0.3s ease 0s;
  width: 0;
}
.heading:hover:after {
  width: 100%;
  left: 0;
}
/* Portrait and Landscape */
@media only screen and (min-device-width: 375px) and (max-device-width: 667px) and (-webkit-min-device-pixel-ratio: 2) {
  .image {
    height: 30vh;
    margin-top: -30px;
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
  .paragraph {
    font-size: 12px !important;
    line-height: 1.2 !important;
  }
  .paragraph2 {
    font-size: 10px !important;
    line-height: 1.2 !important;
  }
  .heading {
    margin-bottom: -25px !important;
    margin-top: -30px !important;
  }
  h3 {
    font-size: 16px;
  }
  .card {
    height: 90vh !important;
  }
  .hobbies {
    margin-top: 40px !important;
  }
}
@media only screen and (min-device-width: 414px) and (max-device-width: 736px) and (-webkit-min-device-pixel-ratio: 3) {
  .image {
    height: 30vh;
    margin-top: -30px;
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
  .paragraph {
    font-size: 14px !important;
    line-height: 1.2 !important;
  }
  .paragraph2 {
    font-size: 12px !important;
    line-height: 1.2 !important;
  }
  .heading {
    margin-bottom: -25px !important;
    margin-top: -30px !important;
  }
  h3 {
    font-size: 16px;
  }
  .card {
    height: 90vh !important;
  }
  .hobbies {
    margin-top: 40px !important;
  }
}
@media only screen and (min-device-width: 375px) and (max-device-width: 812px) and (-webkit-min-device-pixel-ratio: 3) {
  .image {
    height: 30vh;
    margin-top: -30px;
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
  .paragraph {
    font-size: 14px !important;
    line-height: 1.2 !important;
  }
  .paragraph2 {
    font-size: 12px !important;
    line-height: 1.2 !important;
  }
  .heading {
    margin-bottom: -25px !important;
    margin-top: -30px !important;
  }
  h3 {
    font-size: 16px;
  }
  .card {
    height: 90vh !important;
  }
  .hobbies {
    margin-top: 40px !important;
  }
}
@media only screen and (min-device-width: 768px) and (max-device-width: 1024px) and (-webkit-min-device-pixel-ratio: 1) {
  .image {
    height: 35vh;
    margin-top: -30px;
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
  .paragraph {
    font-size: 14px !important;
    line-height: 1.2 !important;
  }
  .paragraph2 {
    font-size: 12px !important;
    line-height: 1.2 !important;
  }
  .heading {
    margin-bottom: -25px !important;
    margin-top: -30px !important;
  }
  h3 {
    font-size: 16px;
  }
  .card {
    height: 90vh !important;
  }
  .hobbies {
    margin-top: 40px !important;
  }
}
</style>
