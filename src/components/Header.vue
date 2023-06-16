<template>
  <div>
    <v-toolbar flat height="80" min-width="350" class="" >
      <v-toolbar-title class="ftleft hidden-sm-and-down">
        <li ><a href="#">Cozy<span>&reg;</span></a></li>
      </v-toolbar-title>
      <v-spacer class="hidden-sm-and-down"></v-spacer>

      <v-toolbar-items class="ftcenter align-center hidden-sm-and-down">
        <li><a href="#">Shop</a></li>
        <li><a href="#">Collective</a></li>
        <li><a href="#">Designers</a></li>
        <li><a class="text-no-wrap" href="#">About Us</a></li>
        <li><a href="#">Contact</a></li>
      </v-toolbar-items>
      <v-spacer class="hidden-sm-and-down"></v-spacer>

      <v-toolbar-items class="d-flex align-center justify-center mx-auto">
        <v-menu
          open-on-hover
          width="30%"
          offset-y>
          <template v-slot:activator="{ on, attrs }">
          <li class="px-0">
            <v-hover v-slot="{hover}">
              <v-btn v-bind="attrs" v-on="on" :style="{'background-color':hover ? '#FFB84C' : '#FFFFFF'}" width="40" height="40" text><img width="25" height="25" src="../assets/menu 1.png">
              </v-btn>
            </v-hover>
          </li>
          </template>

          <v-list>
            <v-list-item-title>
            <div>
            <li><v-btn @click="home" text><a class="" href="#">Shop</a></v-btn></li>
            </div>
            
            <div>
            <li><v-btn @click="about" text><a href="#">Collective</a></v-btn></li>
            </div>

            <div>
            <li><v-btn @click="contact" text><a href="#">Designers</a></v-btn></li>
            </div>

            <div>
            <li><v-btn @click="size" text><a href="#">About Us</a></v-btn></li>
            </div>

            <div>
            <li><v-btn @click="hto" text><a href="#">Contact</a></v-btn></li>
            </div>
            </v-list-item-title>
          </v-list>
        </v-menu>

        <li class="px-0">
          <v-hover v-slot="{hover}">
            <v-btn id="bgcolor" :style="{'background-color':hover ? '#FFB84C' : '#FFFFFF'}" width="40" height="40" text><img width="25" height="25" src="../assets/search.png">
            </v-btn>
          </v-hover>
        </li>
        <v-divider class="mx-4 hidden-sm-and-down" vertical></v-divider>
        <li class="px-0">
          <v-hover v-slot="{hover}">
            <v-btn id="bgcolor" :style="{'background-color':hover ? '#FFB84C' : '#FFFFFF'}" width="40" height="40" text><img width="25" height="25" src="../assets/shopping-cart.png">
            </v-btn>
          </v-hover>
        </li>
      </v-toolbar-items>
    </v-toolbar>
    <v-divider></v-divider>
  </div>
      
</template>

<script>

export default {

  name: 'header-page',

  data (){
    return{

    }
  },

  methods : {

  },

  created(){

  },
}
</script>

<style>
.body{
  position: relative;
  height: 100%;
  width:100%;
}

.ftleft{
  font-family: cambay;
  font-style: normal;
  font-weight: 700;
  font-size: 24px;
  line-height: 39px;
  text-transform: capitalize;
  color: #17183B;
}

.ftcenter{
  font-family:proxima;
  font-style: normal;
  font-weight: 600;
  font-size: 14px;
  line-height: 14px;
  text-transform: uppercase;
  color: #17183B;
}

.fw-xs{
  font-size: 15px; 
  font-style: normal;
  font-weight: 500;
  text-transform: uppercase;
  padding: 20px 15px;
  justify-content: left;
  letter-spacing: 0.08em;
}

li{
  display: inline; 
  padding: 0px 20px;
}

a{
  color:black!important;
  text-decoration:none;
}

a:hover{
  color: #FFB84C!important;
}


</style>
