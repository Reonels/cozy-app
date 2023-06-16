<template>
  <div class="body fill-height">
    <v-row>
      <v-col class="d-flex colpro1 ps-0" cols="12" lg="5">
        <div>
          <v-row class="marpro1 flex-nowrap">
            <div class="ps-1">
              <v-icon large color="black">
                mdi-arrow-left-thin
              </v-icon>
            </div>

            <div class="d-flex d-sm-none justify-center align-center text-right ms-10 px-0">
              <v-btn class="px-0" plain width="20" height="20"><a href="https://www.facebook.com/" target="_blank"><img width="16" height="16" src="../assets/facebook.png"></a></v-btn>
              <v-btn class="px-0" plain width="20" height="20"><a href="https://twitter.com/" target="_blank"><img width="16" height="16" src="../assets/twitter.png"></a></v-btn>
              <v-btn class="px-0" plain width="20" height="20"><a href="https://id.pinterest.com/" target="_blank"><img width="16" height="16" src="../assets/pinterest.png"></a></v-btn>
              <v-btn class="px-0" plain width="20" height="20"><a href="https://www.instagram.com/" target="_blank"><img width="16" height="16" src="../assets/instagram.png"></a></v-btn>
            </div>
          </v-row>

          <div class="marpro2">
            <p class="fs"><span style="opacity: 0.4;">{{ item.type }} </span> / Meryl Lounge Chair</p>
          </div>

          <div class="marpro3">
            <p class="fs4" v-html="item.name"></p>
          </div>

          <div class="marpro4">
            <v-row class="flex-column">
              <v-col class="d-flex align-center">
                <div>
                <p class="fs2 mb-0 text-no-wrap">$ {{ item.price }}</p>
                </div>

                <div class="ms-15 hidden-xs-only">
                  <v-rating
                    background-color="grey lighten-1"
                    color="#F8C420"
                    half-increments
                    hover
                    length="5"
                    size="15"
                    v-model="item.rate"
                    readonly
                    dense
                  >
                  </v-rating>
                </div>

                <div class="hidden-xs-only">
                  <p class="fs my-auto mx-2 text-no-wrap">{{ item.rate }} / 5.0 
                  <span style="opacity: 0.4;">( {{ item.totrate }} )</span></p>
                </div>
              </v-col>

              <v-col class="hidden-sm-and-up">
                <v-row class="ms-1">
                  <v-rating
                    background-color="grey lighten-1"
                    color="#F8C420"
                    half-increments
                    hover
                    length="5"
                    size="15"
                    v-model="item.rate"
                    readonly
                    dense
                  >
                  </v-rating>

                  <p class="fs my-auto mx-2">{{ item.rate }} / 5.0 
                    <span style="opacity: 0.4;">( {{ item.totrate }} )</span></p>
                </v-row>
              </v-col>
            </v-row>
          </div>

          <div class="manpro5">
            <p class="fs3 text-no-wrap" v-html="item.description"></p>
          </div>

          <div class="manpro6">
            <v-card flat class="">
              <v-btn fab class="me-2" width="20" height="20" v-for="(color,index) in item.colors" :key="index" :value="index" :color="item.colors[index].value" >
              </v-btn>
            </v-card>
          </div>

          <div class="manpro7">
            <v-row class="ps-3">
              <v-card outlined min-width="140" max-width="160" height="52" class="d-flex flex-nowrap justify-center align-center cardpro me-6">
                <v-btn fab small class="" text><v-icon>mdi-minus</v-icon></v-btn>
                <p class="fs3 mb-0 align-center mx-6">{{ quantity }}</p>
                <v-btn fab small text><v-icon>mdi-plus</v-icon></v-btn>
              </v-card>

              <div class="">
                <v-btn style="color: white;" class="fs" max-width="200" height="52" color="#44A39F">
                  Add To Cart
                </v-btn>
              </div>

              <!-- <v-col>
                <v-btn style="color: white;" class="fs" max-width="200" height="52" color="#44A39F">
                  Add To Cart
                </v-btn>
              </v-col> -->
            </v-row>
          </div>

          <div class="manpro8">
            <p class="fs3">Free 2-5 day shipping <br class="hidden-sm-and-up">
              <v-icon color="black">mdi-circle-small</v-icon> Tool-free assembly <br class="hidden-sm-and-up">
              <v-icon color="black">mdi-circle-small</v-icon> 30-day trial</p>
          </div>

          <div class="manpro9">
            <v-row class="">
              
                <div>
                  <v-btn elevation="0" @click="toggle" style="color: #3AA39F;text-transform: capitalize;background-color: white;" class="d-flex align-center fs3 px-2">
                    <v-icon  color="#3AA39F">
                      {{iconfav}}
                    </v-icon>
                    <p class="mb-0 ms-4">Add To Wishlist</p>
                  </v-btn>
                </div>

                <div class="my-auto ms-10 px-0 hidden-xs-only">
                  <v-btn class="px-0" plain width="20" height="20"><a href="https://www.facebook.com/" target="_blank"><img width="16" height="16" src="../assets/facebook.png"></a></v-btn>
                  <v-btn class="px-0" plain width="20" height="20"><a href="https://twitter.com/" target="_blank"><img width="16" height="16" src="../assets/twitter.png"></a></v-btn>
                  <v-btn class="px-0" plain width="20" height="20"><a href="https://id.pinterest.com/" target="_blank"><img width="16" height="16" src="../assets/pinterest.png"></a></v-btn>
                  <v-btn class="px-0" plain width="20" height="20"><a href="https://www.instagram.com/" target="_blank"><img width="16" height="16" src="../assets/instagram.png"></a></v-btn>
                </div>
              

              <!-- <v-col class="d-flex align-center justify-start px-0">
                <v-btn class="px-0" plain width="20" height="20"><img width="16" height="16" src="../assets/facebook.png"></v-btn>
                <v-btn class="px-0" plain width="20" height="20"><img width="16" height="16" src="../assets/twitter.png"></v-btn>
                <v-btn class="px-0" plain width="20" height="20"><img width="16" height="16" src="../assets/pinterest.png"></v-btn>
                <v-btn class="px-0" plain width="20" height="20"><img width="16" height="16" src="../assets/instagram.png"></v-btn>
              </v-col> -->
            </v-row>
          </div>
        </div>
      </v-col>
      

      <v-col cols="12" lg="6">
        <div class="text-right manpro10">
          <p style="font-weight: bold;" class="fs2"> 0<span>{{ model + 1 }}</span> <sup><span class="fs5">/ 05</span></sup></p>
        </div>

        <div class="">
          

          <div>
            <v-card flat>
              <div class="text-right manpro11">
                <v-icon text @click="model--" class="" large>
                  mdi-chevron-left
                </v-icon>
                <v-icon @click="model++" class="colpro1" large>
                  mdi-chevron-right
                </v-icon>
              </div>

              <v-carousel
              v-model="model"
              :show-arrows="false"
              hide-delimiters
              height="470"
              >
                <v-carousel-item
                src="../assets/Rectangle 1.png"
                max-width="100%"
                height="auto"
                style = "transition: 1s ease;"
                contain
                >
                </v-carousel-item>

                <v-carousel-item
                src="../assets/Rectangle 2.png"
                max-width="100%"
                height="auto"
                style = "transition: 1s ease;"
                contain
                >
                </v-carousel-item>

                <v-carousel-item
                src="../assets/Rectangle 3.png"
                max-width="100%"
                height="auto"
                style = "transition: 1s ease;"
                contain
                >
                </v-carousel-item>

                <v-carousel-item
                src="../assets/Rectangle 4.png"
                max-width="100%"
                height="auto"
                style = "transition: 1s ease;"
                contain
                >
                </v-carousel-item>

                <v-carousel-item
                src="../assets/Rectangle 5.png"
                max-width="100%"
                height="auto"
                style = "transition: 1s ease;"
                contain
                >
                </v-carousel-item>
              </v-carousel>
            </v-card>
          </div>

          <!-- <v-img class="mx-auto" width="470" height="470" src= "../assets/Rectangle 1.png" >
            
          </v-img> -->
        </div>

        <div class="marpro2">
          <v-row class="d-flex justify-center align-center">
            <v-col>
              <v-card @click="model = 0" outlined elevation="0" class="mx-3 cardpro2">
                <v-img contain class="mx-auto" min-width="50" min-height="50" width="104" height="104" src= "../assets/Rectangle 1.png" ></v-img>
              </v-card>
            </v-col>

            <v-col>
              <v-card @click="model = 1" outlined elevation="0" class="mx-3 cardpro2">
              <v-img contain class="mx-auto" width="104" height="104" src= "../assets/Rectangle 2.png" ></v-img>
              </v-card>
            </v-col>

            <v-col>
              <v-card @click="model = 2" outlined elevation="0" class="mx-3 cardpro2">
              <v-img contain class="mx-auto" width="104" height="104" src= "../assets/Rectangle 3.png" ></v-img>
              </v-card>
            </v-col>

            <v-col>
              <v-card @click="model = 3" outlined elevation="0" class="mx-3 cardpro2">
              <v-img contain class="mx-auto" width="104" height="104" src= "../assets/Rectangle 4.png" ></v-img>
              </v-card>
            </v-col>

            <v-col>
              <v-card @click="model = 4" outlined elevation="0" class="mx-3 cardpro2">
              <v-img contain class="mx-auto" width="104" height="104" src= "../assets/Rectangle 5.png" ></v-img>
              </v-card>
            </v-col>
          </v-row>
        </div>

      </v-col>
    </v-row>
  </div>
</template>

<script>

export default {
  name: 'home-page',
  components : {

  },

  data (){
    return{
      items : [],
      type : "",
      name : "",
      description : "",
      rate : "",
      price : "",
      totrate : "",
      select : "",
      quantity : 1,
      model : 0,
      iconfav : "mdi-heart-outline",
      item : {
        type : "Chair",
        name : "Meryl Lounge <br class='hidden-sm-and-up'>Chair",
        rate : "4.6",
        price : "149.99",
        totrate : "556",
        colors :[
        { value: '#C1BDB3' }, // primary
        { value: '#58737D' }, // secondary
        { value: '#545454' }, // accent
        { value: '#CBA5A5' }, // error
        ],
        description :"The gently curved lines accentuated by sewn <br class='hidden-sm-and-up'>details are kind <br class='hidden-xs-only'> to your body and pleasant <br class='hidden-sm-and-up'> to look at. Also, there's a tilt <br class='hidden-sm-and-up'> and <br class='hidden-xs-only'> height-adjusting mechanism that's built to <br class='hidden-sm-and-up'>outlast years of <br class='hidden-xs-only'> ups and downs.",
      },
    }
  },

  methods : {
    check(x){
      console.log("The Value : ",x);
    },

    toggle(){
      if (this.iconfav === "mdi-heart-outline"){
        this.iconfav = "mdi-heart"
      }
      else if (this.iconfav === "mdi-heart"){
        this.iconfav = "mdi-heart-outline"
      }
      else{
        this.iconfav = "mdi-heart-outline"
      }
    }
  },

  created(){

  }

}

</script>

<style>

</style>