<template>
  <div class="body fill-height">
    <div class="" v-if="true">
      <Header></Header>
    </div>

    <div class="" v-if="true">
      <Product></Product>
    </div>

    <div>

    </div>

    <div>

    </div>

    <div>

    </div>

    <div>

    </div>
    
  </div>
</template>

<script>
import header from '../components/Header.vue';
import product from '../components/Product.vue'

  export default {
    name: 'home-page',
    components : {
      'Header':header,
      'Product':product,
    },

  data (){
    return{

    }
  },

  methods : {

  },

  created(){

  }

  }

</script>

<style>
.fs{
  font-family: proxima;
  font-style: normal;
  font-weight: 600;
  font-size: 14px!important;
  line-height: 14px;
  color: #17183B;
}

.fs2{
  font-family: proxima;
  font-style: normal;
  font-weight: 400;
  font-size: 34px;
  line-height: 34px;
  color: #17183B;
}

.fs3{
  font-family: proxima;
  font-style: normal;
  font-weight: 400;
  font-size: 16px!important;
  line-height: 24px;
  color: #17183B;
}

.fs4{
  font-family: proxima;
  font-style: normal;
  font-weight: bold;
  font-size: 44px;
  line-height: 44px;
  letter-spacing: 0.02em;
  color: #17183B;
}

.fs5{
  font-family: proxima;
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  line-height: 20px;
  color: #17183B;
}

.cardpro{
  border: 1px solid #17183B;
  border-radius: 2px;
}

.cardpro2{
  background: #FFFFFF;
  border: 2px solid #E7ECEF !important;
}

.colpro1{
  margin-left: 80px;
}

.marpro1{
  margin-top: 60px;
}

.marpro2{
  margin-top: 40px;
}

.marpro3{
  margin-top: 76px;
}

.marpro4{
  margin-top: 29px;
}

.manpro5{
  margin-top: 44px;
}

.manpro6{
  margin-top: 34px;
}

.manpro7{
  margin-top: 36px;
}

.manpro8{
  margin-top: 32px;
}

.manpro9{
  margin-top: 88px;
}

.manpro10{
  margin-top: 64px;
  margin-right: 86px;
}

.manpro11{
  margin-top: 21px;
  margin-right: 40px;
}

.manpro12{
  margin-top : 21px;
}

@media only screen and (max-width:1264px){
  .colpro1{
    justify-content:center;
  }

}

@media only screen and (max-width:960px){
  .colpro1{
    margin-left:auto;
    justify-content:center;
  }
}

@media only screen and (max-width:600px){
  .colpro1{
    margin-left:30px;
    justify-content:left;
  }

}
</style>