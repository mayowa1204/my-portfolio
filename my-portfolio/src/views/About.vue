<template>
  <div style=" background-image: linear-gradient(to right, #e6e6fa, white);">
    <section class="mx-auto" style="height:70vh;  ">
      <v-row style="width:100%;height:100%;margin-top:100px" class="mx-auto">
        <v-card style="width:90%;height:100%" class="mx-auto ">
          <v-row style="height:90%" wrap no-gutters>
            <v-col cols="12" md="6" class="image">
              <v-img
                class=" picture mx-auto mt-10"
                height="400px"
                width="400px"
                aspect-ratio="1"
                src="../assets/me-main.jpg"
              >
              </v-img>
            </v-col>
            <v-col cols="12" md="6" style="height:100%">
              <div class="mx-auto" style="width:90%">
                <h2 class="mt-10" style="text-align:center">About Me</h2>
                <p class="mt-10" style="text-align:justify">
                  Lorem ipsum, dolor sit amet consectetur adipisicing elit. Odio
                  natus numquam quia eaque voluptate cumque? Tempore debitis
                  voluptates saepe facilis ea eum! Blanditiis dolorum ipsum
                  recusandae rem. Quae, eius asperiores.
                </p>
              </div>
            </v-col>
          </v-row>
        </v-card>
      </v-row>
    </section>
    <section class="mx-auto" style="height:70vh">
      <v-row class="mx-auto" style="width:100%;height:100%;margin-top:100px">
        <v-card style="width:90%;height:100%" class="mx-auto">
          <v-row style="height:90%">
            <v-col cols="12" md="6" class=" image">
              <v-img
                class="picture mx-auto mt-10"
                height="400px"
                width="400px"
                aspect-ratio="1"
                src="../assets/me-main.jpg"
              >
              </v-img>
            </v-col>
            <v-col cols="12" md="6">
              <div class="mx-auto" style="width:90%">
                <h2 class="mt-10" style="text-align:center">Education</h2>
                <p class="mt-10" style="text-align:justify">
                  Lorem ipsum dolor sit, amet consectetur adipisicing elit. Nemo
                  nisi vel laborum quisquam, repellat ab reprehenderit ea
                  excepturi expedita? Autem numquam perferendis dicta veniam
                  sint, quod aspernatur reiciendis ex rem?
                </p>
              </div></v-col
            >
          </v-row>
        </v-card>
      </v-row>
    </section>
    <section style="height:70vh;">
      <v-row class="mx-auto" style="width:100%;height:100%;margin-top:100px">
        <v-card style="width:90%;height:100%" class="mx-auto">
          <v-row style="height:90%">
            <v-col cols="12" md="6" class=" image">
              <v-img
                class="picture mx-auto mt-10"
                height="400px"
                width="400px"
                aspect-ratio="1"
                src="../assets/me-main.jpg"
              >
              </v-img>
            </v-col>
            <v-col cols="12" md="6">
              <div class="mx-auto" style="width:90%">
                <h2 class="mt-10" style="text-align:center">Hobbies</h2>
                <p class="mt-10" style="text-align:jsutify">
                  Lorem ipsum, dolor sit amet consectetur adipisicing elit. Cum
                  nemo asperiores non ipsa doloremque praesentium expedita unde
                  consectetur nam! Consequuntur facilis quae quibusdam molestiae
                  rem accusantium qui nostrum quis exercitationem!
                </p>
              </div>
            </v-col>
          </v-row>
        </v-card>
      </v-row>
    </section>
    <section class="mx-auto" style="height:70vh; margin-bottom:100px ">
      <v-row class="mx-auto" style="width:100%;height:100%;margin-top:100px">
        <v-card style="width:90%;height:100%;" class="mx-auto">
          <v-row style="height:90%">
            <v-col cols="12" md="6" class=" image">
              <v-img
                class="picture mx-auto mt-10"
                height="400px"
                width="400px"
                aspect-ratio="1"
                src="../assets/me-main.jpg"
              >
              </v-img>
            </v-col>
            <v-col cols="12" md="6">
              <div class="mx-auto" style="width:90%">
                <h2 class="mt-10" style="text-align:center">Travel</h2>
                <p class="mt-10" style="text-align:justify">
                  Lorem ipsum dolor sit amet consectetur adipisicing elit.
                  Debitis quibusdam perferendis illum distinctio, qui fugit
                  alias sint maiores nobis deserunt impedit eligendi consectetur
                  soluta asperiores doloribus voluptatibus error voluptate
                  mollitia.
                </p>
              </div></v-col
            >
          </v-row>
        </v-card>
      </v-row>
    </section>
  </div>
</template>
<style scoped>
/* Portrait and Landscape */
@media only screen and (min-device-width: 375px) and (max-device-width: 667px) and (-webkit-min-device-pixel-ratio: 2) {
  .image {
    height: 30%;
  }
  .picture {
    height: 100px !important;
    width: 100px !important;
  }
}
@media only screen and (min-device-width: 414px) and (max-device-width: 736px) and (-webkit-min-device-pixel-ratio: 3) {
  .image {
    height: 30%;
  }
  .picture {
    height: 100px !important;
    width: 100px !important;
  }
}
@media only screen and (min-device-width: 375px) and (max-device-width: 812px) and (-webkit-min-device-pixel-ratio: 3) {
  .image {
    height: 30%;
  }
  .picture {
    height: 100px !important;
    width: 100px !important;
  }
}
@media only screen and (min-device-width: 768px) and (max-device-width: 1024px) and (-webkit-min-device-pixel-ratio: 1) {
  .image {
    height: 35%;
  }
  .picture {
    height: 200px !important;
    width: 200px !important;
  }
}
</style>
