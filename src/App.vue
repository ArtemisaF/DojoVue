<template>
  <v-conten>
    <Toolbar></Toolbar>
    <Busquedad></Busquedad>
    <ImagenList></ImagenList>
  </v-conten>
</template>

<script>
import Toolbar from './components/Toolbar';
import Busquedad from './components/Busquedad';
import  ImagenList from './components/ImagenList'

export default {
  name: 'App',

  components: {
    Toolbar,
    Busquedad,
    ImagenList
  },

  data: () => ({
    //
  }),
};
</script>
