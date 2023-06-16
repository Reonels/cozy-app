<template>
  <v-app>
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>


<script>
export default {
  name: 'App',

  data: () => ({
    //
  }),
}
</script>

<style>
@font-face{
  font-family: proxima;
  src: url(@/font/Proxima/Proxima\ Nova\ Regular.otf);
  font-style: normal;
  font-weight: normal;
}

@font-face{
  font-family: proxima;
  src: url(@/font/Proxima/Proxima\ Nova\ Regular\ Italic.otf);
  font-style: italic;
  font-weight: normal;
}

@font-face{
  font-family: proxima;
  src: url(@/font/Proxima/Proxima\ Nova\ Bold.otf);
  font-style: normal;
  font-weight: bold;
}

@font-face{
  font-family: cambay;
  src: url(@/font/Cambay/Cambay-Regular.ttf);
  font-style: normal;
  font-weight: normal;
}

</style>
