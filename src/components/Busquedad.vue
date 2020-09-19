<template>
  <v-container fluid>
    <v-textarea
        autocomplete=" "
        label="Busquedad"
    ></v-textarea>
    <div class="text-center">
      <v-btn class="mx-5" fab dark small color="primary">

        <v-icon dark>Go!</v-icon>
      </v-btn>
    </div>
  </v-container>
</template>
<scrip>
import axios from 'axios';
export default{
  name:"Busquedad",
  data:() =>({
    search:[],
    word:''

  }),
  methods: {
    searchItem () {
        axios
          .get(
              "https://pixabay.com/api/?key=18325849-94cafec8b0f30985ae8cfbdde&q="+this.word+"&image_type=photo"
          )
          .then((response)=>{
              this.search= response.date;
              console.log(this.search);
          });
    },
  },
};
</scrip>