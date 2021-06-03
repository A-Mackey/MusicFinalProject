<template>
  <div>

    <!-- Pic & Title -->
    <v-container>
      <v-row class="text-center" align="center" cols="12">

        <!-- Logo -->
        <v-col cols="12" sm="6" md="6" lg="6" xl="6">
          <v-img
            :src="require('@/assets/Pictures/Dancing.svg')"
            class=""
            contain
            height="400"
          />
        </v-col>

        <!-- Header Text -->
        <v-col cols="12" sm="6" md="6" lg="6" xl="6">
          <h1 class="display-2 mb-3 webTitle">
            {{Title}}
          </h1>

          <p class="subheading font-weight-regular" style="font-size: 1.25em;">
            {{SubTitle}}
            <a
              href="https://open.spotify.com/playlist/7aXPUKyzOLHm3QSz8M5po1?si=bf262a4693d348ed"
              target="_blank"
            >Spotify Playlist</a>
          </p>

          <p
            class="disclaimer"
          >{{Disclaimer}}</p>
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
          <p>{{CultureTextp1}}</p>
          <br>
          <p>{{CultureTextp2}}</p>
          <br>
          <p>{{CultureTextp3}}</p>
        </v-col>
      </v-row>
    </v-container>

    <!-- <v-divider
      class="mt-5 mb-5 mr-12 ml-12"
      :inset="inset"
      
    ></v-divider> -->

    
    <v-container class="mt-6 mb-6">
      <v-row cols="12">

        <!-- Header Text -->
        <v-col cols="12" sm="6" md="6" lg="6" xl="6">
          <p class="text-right">{{CultureHistoryTextp1}}</p>
          <br>
          <p class="text-right">{{CultureHistoryTextp2}}</p>
          <br>
          <p class="text-right">{{CultureHistoryTextp3}}</p>
          <br>
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
              {{CultureHistory}}
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

    <!-- Parralax (Artists Divider) -->
    <v-parallax 
      :src=ArtistPicture
      height="300"
    > 
      <h1
        class="text-center parallexTitle"
      >Artists</h1>  
    </v-parallax>

    <!-- Artist 1 -->
    <v-container class="mt-6">
      <v-row cols="12">

        <!-- Logo -->
        <v-col cols="12" sm="6" md="6" lg="6" xl="6">
          <v-card 
            flat color="#white" 
            style="border-radius: 0%;"
            data-aos="fade-left"
            data-aos-duration="500" 
            data-aos-delay="50"
          >
            <h1
              class="text-right mr-4 sectionHeader"
              
            >
              {{Artist1}}
            </h1>

            <v-row  justify="center">
              <v-col cols="8">
                <vuetify-audio flat :file="Artist1Audio" color="black" :ended="audioFinish" />

              </v-col>
            </v-row>
          </v-card>
        </v-col>

        <v-divider
          class=""
          :inset="inset"
          vertical
        ></v-divider>

        <!-- Header Text -->
        <v-col cols="12" sm="6" md="6" lg="6" xl="6" 
          data-aos="fade-right"
          data-aos-duration="500" 
          data-aos-delay="50"
        >
          <p>{{Artist1Text}}</p>
        </v-col>
      </v-row>
    </v-container>

    <!-- Artist 2 -->
    <v-container class="mt-6 mb-6">
      <v-row cols="12">

        <!-- Header Text -->
        <v-col cols="12" sm="6" md="6" lg="6" xl="6" 
          data-aos="fade-left"
          data-aos-duration="500" 
          data-aos-delay="50"  
        >
          <p
            class="text-right"
          >
          {{Artist2Text}}</p>
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
            data-aos="fade-right"
            data-aos-duration="500" 
            data-aos-delay="50"
          >
            <h1
              class="text-left mr-4 sectionHeader"
            >
              {{Artist2}}
            </h1>

            <v-row  justify="center">
              <v-col cols="8">
                <vuetify-audio flat :file="Artist2Audio" color="black" :ended="audioFinish" />

              </v-col>
            </v-row>

          </v-card>
        </v-col>
      </v-row>
    </v-container>

    <!-- Artist 3 -->
    <v-container class="mt-6">
      <v-row cols="12">

        <!-- Logo -->
        <v-col cols="12" sm="6" md="6" lg="6" xl="6">
          <v-card 
            flat color="#white" 
            style="border-radius: 0%;"
            data-aos="fade-left"
            data-aos-duration="500" 
            data-aos-delay="50"
          >
            <h1
              class="text-right mr-4 sectionHeader"
              
            >
              {{Artist3}}
            </h1>

            <v-row  justify="center">
              <v-col cols="8">
                <vuetify-audio flat :file="Artist3Audio" color="black" :ended="audioFinish" />

              </v-col>
            </v-row>
          </v-card>
        </v-col>

        <v-divider
          class=""
          :inset="inset"
          vertical
        ></v-divider>

        <!-- Header Text -->
        <v-col cols="12" sm="6" md="6" lg="6" xl="6" 
          data-aos="fade-right"
          data-aos-duration="500" 
          data-aos-delay="50"
        >
          <p>{{Artist3Text}}</p>
        </v-col>
      </v-row>
    </v-container>

    <!-- Artist 4 -->
    <v-container class="mt-6 mb-6">
      <v-row cols="12">

        <!-- Header Text -->
        <v-col cols="12" sm="6" md="6" lg="6" xl="6"  
          data-aos="fade-left"
          data-aos-duration="500" 
          data-aos-delay="50"
        >
          <p
            class="text-right"
          >
          {{Artist4Text}}</p>
        </v-col>

        <v-divider
          class=""
          :inset="inset"
          vertical
        ></v-divider>
        
        <!-- Logo -->
        <v-col cols="12" sm="6" md="6" lg="6" xl="6" 
          data-aos="fade-right"
          data-aos-duration="500" 
          data-aos-delay="50"  
        >
          <v-card 
            flat color="#white" 
            style="border-radius: 0%;"
          >
            <h1
              class="text-left mr-4 sectionHeader"
              
            >
              {{Artist4}}
            </h1>

            <v-row  justify="center">
              <v-col cols="8">
                <vuetify-audio flat :file="Artist4Audio" color="black" :ended="audioFinish" />

              </v-col>
            </v-row>

          </v-card>
        </v-col>
      </v-row>
    </v-container>

    <!-- Artist 5 -->
    <v-container class="mt-6 mb-6">
      <v-row cols="12">

        <!-- Title & Stuff -->
        <v-col cols="12" sm="6" md="6" lg="6" xl="6">
          <v-card 
            flat color="#white" 
            style="border-radius: 0%;"
            data-aos="fade-left"
            data-aos-duration="500" 
            data-aos-delay="50"
          >
            <h1
              class="text-right mr-4 sectionHeader"
              
            >
              {{Artist5}}
            </h1>

            <v-row  justify="center">
              <v-col cols="8">
                <vuetify-audio flat :file="Artist5Audio" color="black" :ended="audioFinish" />

              </v-col>
            </v-row>
          </v-card>
        </v-col>

        <v-divider
          class=""
          :inset="inset"
          vertical
        ></v-divider>

        <!-- Header Text -->
        <v-col cols="12" sm="6" md="6" lg="6" xl="6" 
          data-aos="fade-right"
          data-aos-duration="500" 
          data-aos-delay="50"  
        >
          <p>{{Artist5Text}}</p>
        </v-col>
      </v-row>
    </v-container>

    <!-- Artist 6 -->
    <v-container class="mt-6 mb-6">
      <v-row cols="12">

        <!-- Header Text -->
        <v-col cols="12" sm="6" md="6" lg="6" xl="6"  
          data-aos="fade-left"
          data-aos-duration="500" 
          data-aos-delay="50"
        >
          <p
            class="text-right"
          >
          {{Artist6Text}}</p>
        </v-col>

        <v-divider
          class=""
          :inset="inset"
          vertical
        ></v-divider>
        
        <!-- Logo -->
        <v-col cols="12" sm="6" md="6" lg="6" xl="6" 
          data-aos="fade-right"
          data-aos-duration="500" 
          data-aos-delay="50"  
        >
          <v-card 
            flat color="#white" 
            style="border-radius: 0%;"
          >
            <h1
              class="text-left mr-4 sectionHeader"
              
            >
              {{Artist6}}
            </h1>

            <v-row  justify="center">
              <v-col cols="8">
                <vuetify-audio flat :file="Artist4Audio" color="black" :ended="audioFinish" />

              </v-col>
            </v-row>

          </v-card>
        </v-col>
      </v-row>
    </v-container>

     <!-- Concluding Statement -->
    <v-row 
      cols="12" 
      justify="center" 
      class="text-center mt-6 mb-6"
    >
      <v-col cols="12" md="8" lg="8" xl="8">

        <v-card flat>
          <h1>{{ConclusionTitle}}</h1>
          <p>
            {{ConclusionText}}
          </p>
        </v-card>

      </v-col>
    </v-row>


    <!-- Parralax (Artists Divider) -->
    <v-parallax 
      :src=PersonalStatementPicture
      height="300"
      class="text-center"
    > 
      <h1
        class="parallexTitle"
      >
      Personal Statement
      </h1>  
    </v-parallax>

    <!-- Personal Statement -->
    <v-row 
      cols="12" 
      justify="center" 
      class="text-center mt-6 mb-6"
    >
      <v-col cols="12" md="8" lg="8" xl="8">

        <v-card flat>
          <h1>{{PersonalStatementTitle}}</h1>
          <p>
            {{PersonalStatementText}}
          </p>
        </v-card>

      </v-col>
    </v-row>

    <!-- Bottom Footer -->
    <v-footer>
      <v-card width="100%" flat tile color="rgba(0,0,0,0)">

        <v-card-title>
          <p class="footerText">Thank you for reading</p>

          <v-spacer></v-spacer>

          <p class="footerCopyright">© {{ new Date().getFullYear() }} — <strong>Aidan Mackey</strong></p>
        </v-card-title>

      </v-card>
    </v-footer>

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
      Disclaimer: "Disclaimer: Most of these songs contain profanity so listen at your own digression.",

      Culture: "UK Hip-Hop & Drill Culture Intro",
      CultureTextp1: "I will be discussing and analyzing the drill hip-hop music coming from the United Kingdom. Before we discuss the Drill scene in just the UK, it is important to know a little bit about the history of this Hip-Hop sub-genre. Where did it come from? How did it originate? How has the UK influenced this style of music, today?",
      CultureTextp2: "First, what is drill music? Drill is a style of rap where the beat is made much more aggressive with loud 808's (Base), punchy kicks, and unique hi-hat patterns that give an alternate bounce to the standard 1/2 step patterns common in other kinds of rap music at the time. The vocals are also made much more aggressive and tend to be more melodic than other forms or rap. Compared to other genres at the time, drill rap sounded so much different and certainly stood out from the other styles with its loud and destructive-like sound.",
      CultureTextp3: "Now, let’s discuss where it originated. In 2012, from the heart of Chicago, the early styles of drill rap started to emerge with the rising artist, Chief Keef. He released his debut album \"Finally Rich\", which peaked at #29 on the Billboard Hot 200, with the iconic songs \"Love Sosa\" and \"Hate Bein' Sober\" featured on it. These songs will be heard in the 'Artists' section of this website. From there, drill music continued to live and thrive within the music scene of Chicago until being heard from across the Atlantic and erupted in the UK.",

      CultureHistory: "UK Drill Culture History",
      CultureHistoryTextp1: "Years later, with some evolution to the genre, the style of music traversed all the way across to Eurupe and the drill music style was heard and liked by many underground UK rappers. The first big song to break out in the UK was by the underground rap group named the \"Harlem Spartans\", and the song was \"Kennington Where It Started\" and it was released in early 2017. Kennington is a city south of London and the place where the Harlem Spartans are based. The song was like nothing else that had gone viral within the country and sparked a new drill rap movement throughout all of Europe.",
      CultureHistoryTextp2: "From there, bigger UK rappers started to hop on the trend of this new style of music, and only gained more popularity. Artists like Stormzy, Rico Vondelle,and Headie One lead this stride with their respective songs in later 2017. An example of these songs being \"23\" by Rico Vondelle and Headie One can be heard here on the right.",
      CultureHistoryTextp3: "While drill songs in America tend to rap about gun violence, UK drill rappers fixate upon different topics. This is due to the fact that guns are completely outlawed within the UK. Despite there being no guns, there was and still is a massive blade problem there with knives and even swords and this is what a lot of the rappers tend to focus their songs on among other topics such as girls and money. Below, we will go over the timeline of artists and a preview of their music.",

      musicFile: require("@/assets/Music/23cut.mp3"),

      ArtistPicture: require("@/assets/Pictures/PopSmoke.jpg"),

      Artist1: "Chief Keef",
      Artist2: "Harlem Spartans",
      Artist3: "Headie One",
      Artist4: "Stormzy",
      Artist5: "Pop Smoke",
      Artist6: "CJ",

      Artist1Audio: require("@/assets/Music/Sosa.mp3"),
      Artist2Audio: require("@/assets/Music/Beat2.mp3"),
      Artist3Audio: require("@/assets/Music/Beat3.mp3"),
      Artist4Audio: require("@/assets/Music/Beat4.mp3"),
      Artist5Audio: require("@/assets/Music/Beat5.wav"),

      Artist1Text: "As stated previously, Chief Keef is responsible for the emergence of drill rap and breaking it out of the underground scene of Chicago. The song available on the left is his big breakout song titled \"Love Sosa\", released in late 2012, which still stands as his most popular song to this day. Also stated previously, this song was the first to use an overly aggressive beat with loud bass along with the melodic vocals. For a few years, Chief Keef stood as the only mainstream drill artist until the genre's emergence in the United Kingdom.",
      Artist2Text: "Harlem Spartans",
      Artist3Text: "The one and only one",
      Artist4Text: "All my homies Vossi Bop",
      Artist5Text: "You cannot say Pop and forget the Smoke",
      Artist6Text: "Blue cheese, I swear I'm addicted to blue cheese.",

      ConclusionTitle: "In Conclusion",
      ConclusionText: "This is the end.",

      PersonalStatementPicture: require("@/assets/Pictures/SCU.jpg"),

      PersonalStatementTitle: "What I think",
      PersonalStatementText: "I think that...",
    }),
  }
</script>

<style scoped>

  .webTitle {
    color: black;
    font-family: Roboto, Helvetica, sans-serif;
    font-size: 2em;
    font-weight: 100;
  }

  .disclaimer {
    font-size: 0.75em;
    color: grey;
  }

  .sectionHeader {
    color: #34558b;
    font-family: Roboto, Helvetica, sans-serif;
    font-size: 2em;
    font-weight: 400;
  }

  .parallexTitle {
    color: white;
    font-family: Roboto, Helvetica, sans-serif;
    font-size: 2em;
    font-weight: 300;
  }

  .footerText {
    color: black;
    font-family: Roboto, Helvetica, sans-serif;
    font-size: 1.5em;
    font-weight: 300;
  }

  .footerCopyright {
    color: black;
    font-family: Roboto, Helvetica, sans-serif;
    font-size: 1em;
    font-weight: 300;
  }
</style>
