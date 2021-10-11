<template>
  <v-container class="mt-8">
    <v-row>
        <v-col
          cols="12"
          sm="6"
        >
          <v-text-field
            v-model="indonesia"
            label="Any Language"
            clearable
          ></v-text-field>
        </v-col>
        <v-col
          cols="12"
          sm="6"
        >
          <v-text-field
            :value="english"
            label="English"
            readonly
          ></v-text-field>
        </v-col>

    </v-row>
  </v-container>
</template>

<script>
  export default {
    data: () => ({
      indonesia: '',
      english: '',
      // select engine baidu/google
      engine: 'google',
      // translate to what language, en = english
      to: 'en'
    }),
    methods: {

    },
    watch: {
      indonesia: function(){
        const config = {
          method: 'get',
          url: `https://api-translate.azharimm.site/translate?engine=${this.engine}&text=${this.indonesia}&to=${this.to}`
        }

        this.axios(config)
        .then(response => {
          this.english = response.data.data.result
        })
        .catch(error => {
          console.log(error);
        })
      }
    }
  }
</script>
