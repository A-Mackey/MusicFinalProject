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
            The History of Drill Music in the United Kingdom
          </h1>

          <p class="subheading font-weight-regular">
            For a Spotify playlist of all the songs I will be discussing
            <br>click the link here: 
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
          <v-card width="100%">
            <v-card-title>
              TESTING
            </v-card-title>
          </v-card>
        </v-col>

        <!-- Header Text -->
        <v-col cols="12" sm="6" md="6" lg="6" xl="6">
          <p>TEST TEST TEST TEST</p>
        </v-col>
      </v-row>
    </v-container>


  </div>
</template>

<script>
  export default {
    name: 'HelloWorld',

    data: () => ({

    }),
  }
</script>
