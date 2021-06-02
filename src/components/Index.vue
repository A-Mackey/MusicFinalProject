<template>
  <div>
    <v-container>
      <v-row class="text-center" align="center" cols="12">

        <!-- Logo -->
        <v-col cols="12" sm="6" md="6" lg="6" xl="6">
          <v-img
            :src="require('../assets/Pictures/Dancing.svg')"
            class=""
            contain
            height="400"
          />
        </v-col>

        <!-- Header Text -->
        <v-col cols="12" sm="6" md="6" lg="6" xl="6">
          <h1 class="display-2 font-weight-bold mb-3">
            {{Title}}
          </h1>

          <p class="subheading font-weight-regular" style="font-size: 1.25em;">
            {{SubTitle}}
            <a
              href="https://open.spotify.com/playlist/7aXPUKyzOLHm3QSz8M5po1?si=bf262a4693d348ed"
              target="_blank"
            >Spotify Playlist</a>
          </p>
        </v-col>
      </v-row>
    </v-container>

    <v-container>
      <v-row cols="12">

        <!-- Logo -->
        <v-col cols="12" sm="6" md="6" lg="6" xl="6">
          <v-card 
            flat color="#white" 
            style="border-radius: 0%;"
          >
            <h1
              class="text-right mr-4 sectionHeader"
              
            >
              {{Culture}}
            </h1>
          </v-card>
        </v-col>

        <v-divider
          class=""
          :inset="inset"
          vertical
        ></v-divider>

        <!-- Header Text -->
        <v-col cols="12" sm="6" md="6" lg="6" xl="6">
          <p>{{CultureText}} | {{CultureText}}</p>
        </v-col>
      </v-row>
    </v-container>

    

    <!-- <v-divider
      class="mt-5 mb-5 mr-12 ml-12"
      :inset="inset"
      
    ></v-divider> -->

    
    <v-container class="mt-6">
      <v-row cols="12">

        <!-- Header Text -->
        <v-col cols="12" sm="6" md="6" lg="6" xl="6">
          <p
            class="text-right"
          >
          {{CultureText}} | {{CultureText}}</p>
        </v-col>

        <v-divider
          class=""
          :inset="inset"
          vertical
        ></v-divider>
        
        <!-- Logo -->
        <v-col cols="12" sm="6" md="6" lg="6" xl="6">
          <v-card 
            flat color="#white" 
            style="border-radius: 0%;"
          >
            <h1
              class="text-left mr-4 sectionHeader"
              
            >
              {{Culture}}
            </h1>


            <v-row  justify="center">
              <v-col cols="8">
                <vuetify-audio flat :file="musicFile" color="black" :ended="audioFinish" />

              </v-col>
            </v-row>
            

          </v-card>
        </v-col>

      </v-row>
    </v-container>



  </div>
</template>

<script>

  //Primary Color: #34558b
  import 'vuetify/dist/vuetify.min.css';

  export default {
    name: 'Index',

    components: {
      VuetifyAudio: () => import('vuetify-audio'),
    },

    data: () => ({
      Title: "The History of Drill Music in the United Kingdom",
      SubTitle: "For a Spotify playlist of all the songs I will be discussing click the link here: ",

      Culture: "UK Hip-Hop & Drill Culture",
      CultureText: "A paragraph is a self-contained unit of discourse in writing dealing with a particular point or idea. A paragraph consists of one or more sentences. Though not required by the syntax of any language, paragraphs are usually an expected part of formal writing, used to organize longer prose.",

      musicFile: require("../assets/Music/Beat.mp3"),
    
    }),
  }
</script>

<style scoped>
  .sectionHeader {
    color: #34558b;
    font-family: Arial, Helvetica, sans-serif;
    font-size: 2em;

  }
</style>
