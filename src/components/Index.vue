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
          <p class="disclaimer">
            {{Disclaimer2}}
          </p>
        </v-col>
      </v-row>
    </v-container>

    <!-- Culture -->
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
    
    <!-- History -->
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
          <p>{{Artist5Textp1}}</p>
          <br>
          <p>{{Artist5Textp2}}</p>
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
                <vuetify-audio flat :file="Artist6Audio" color="black" :ended="audioFinish" />

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
          <br>
          <p>
            {{PersonalStatementText2}}
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
      Disclaimer2: "Also, be aware the the music on this website might be loud, so turn your computer volume down to a comftorable level.",

      Culture: "UK Hip-Hop & Drill Culture Intro",
      CultureTextp1: "I will be discussing and analyzing the drill hip-hop music coming from the United Kingdom. Before we discuss the Drill scene in just the UK, it is important to know a little bit about the history of this Hip-Hop sub-genre. Where did it come from? How did it originate? How has the UK influenced this style of music, today?",
      CultureTextp2: "First, what is drill music? Drill is a style of rap where the beat is made much more aggressive with loud 808's (bass), punchy kicks, and unique hi-hat patterns that give an alternate bounce to the standard 1/2 step patterns common in other kinds of rap music at the time. The vocals are also made much more aggressive and tend to be more melodic than other forms or rap. Compared to other genres at the time, drill rap sounded so much different and certainly stood out from the other styles with its loud and destructive-like sound.",
      CultureTextp3: "Now, let’s discuss where it originated. In 2012, from the heart of Chicago, the early styles of drill rap started to emerge with the rising artist, Chief Keef. He released his debut album \"Finally Rich\", which peaked at #29 on the Billboard Hot 200, with the iconic songs \"Love Sosa\" and \"Hate Bein' Sober\" featured on it. These songs will be heard in the 'Artists' section of this website. From there, drill music continued to live and thrive within the music scene of Chicago until being heard from across the Atlantic and erupted in the UK.",

      CultureHistory: "UK Drill Culture History",
      CultureHistoryTextp1: "Years later, with some evolution to the genre, the style of music traversed all the way across to Europe and the drill music style was heard and liked by many underground UK rappers. The first big song to break out in the UK was by the underground rap group named the \"Harlem Spartans\", and the song was \"Kennington Where It Started\" and it was released in early 2017. Kennington is a city south of London and the place where the Harlem Spartans are based. The song was like nothing else that had gone viral within the country and sparked a new drill rap movement throughout all of Europe.",
      CultureHistoryTextp2: "From there, bigger UK rappers started to hop on the trend of this new style of music, and only gained more popularity. Artists like Stormzy, Rico Vondelle, and Headie One lead this stride with their respective songs in later 2017. An example of these songs being \"23\" by Rico Vondelle and Headie One can be heard here on the right.",
      CultureHistoryTextp3: "While drill songs in America tend to rap about gun violence, UK drill rappers fixate upon different topics. This is due to the fact that guns are completely outlawed within the UK. Despite there being no guns, there was and still is a massive blade problem there with knives and even swords and this is what a lot of the rappers tend to focus their songs on among other topics such as girls and money. Below, we will go over the timeline of artists and a preview of their music.",

      musicFile: require("@/assets/Music/23cut.mp3"),

      ArtistPicture: require("@/assets/Pictures/harlemspartans.jpg"),

      Artist1: "Chief Keef",
      Artist2: "Harlem Spartans",
      Artist3: "Headie One",
      Artist4: "Stormzy",
      Artist5: "Pop Smoke",
      Artist6: "CJ",

      Artist1Audio: require("@/assets/Music/Sosa.mp3"),
      Artist2Audio: require("@/assets/Music/harlemspartans.mp3"),
      Artist3Audio: require("@/assets/Music/23cut.mp3"),
      Artist4Audio: require("@/assets/Music/stormzy.mp3"),
      Artist5Audio: require("@/assets/Music/smoke.mp3"),
      Artist6Audio: require("@/assets/Music/cj.mp3"),

      Artist1Text: "As stated previously, Chief Keef is responsible for the emergence of drill rap and breaking it out of the underground scene of Chicago. The song available on the left is his big breakout song titled \"Love Sosa\", released in late 2012, which still stands as his most popular song to this day. Also stated previously, this song was the first to use an overly aggressive beat with loud bass along with the melodic vocals. For a few years, Chief Keef stood as the only mainstream drill artist until the genre's emergence in the United Kingdom.",
      Artist2Text: "Years later, after hearing the style of music that was emerging from Chicago, the Harlem Spartans took it upon themselves to add their own uniqueness to the drill style of music. This is where this genre of music really took off in the UK and where the United Kingdom started to add their own \"spice\" to the style of music. Here, the question of cultural appropriation can be brought up. One could ask, why should these artists on the other side of the world be allowed to copy the unique sound of Chicago's rap scene? Well, as I discussed in my first project of this class, I do not believe there is such thing as cultural appropriation with art. If one artist admires and appreciates the creativity of another artist, they should be able to replicate it themselves and even add their own pieces to the style to contribute to its evolution. In the case of the Harlem Spartans, they certainly did just that. They were able to take the aggressive style of Chicago drill designed by Chief Keef and turn it into a faster-paced style of music with a unique flow, cadence, and bass patterns. From here, the drill style of rap music only evolved further within the United Kingdom after moving from artist to artist over the years. Here on the right is their famous song \"Kennington Where It Started\". Notice the evolution of the hi-hat pattern, snare hits, and dancing 808's throughout the song compared to the style from Chief Keef.",
      Artist3Text: "Further progressing and growing within the United Kingdom, Headie One started to contribute to the genre with his own music. Later that same year, 2017, Headie One released an album titled \"Drillers & Trappers\", which opened up with the drill inspired song \"23\", which is Headie One's first contribution to the style of music. On the left here is the song. Notice the similar hi-hat bounce as well as snare patterns. His difference, however, is the cadence he chooses to sing with. While the Harlem Spartans contributed to the progression of the style of beat's, Headie One was the one to take this contribution from them and combine it with the melodic flows and cadence that were presented by Chief Keef. He essentially blended the two styles, from different parts of the word, into one. Here on the left is his song \"23\"; notice the Chief Keef-like cadence, and Harlem Spartans-like instrumental, as mentioned previously.",
      Artist4Text: "Stormzy is a good representation of where the drill style of music is standing today. Following the trend of the popularity of drill music throughout the United Kingdom, one of the country’s biggest artist's, Stormzy, makes some of the most popular drill music today. Released in 2019, the song \"Vossi Bop\" was a song that really escalated Stormzy to the next level and the song sits with over 240 million plays today. Here on the right is the song \"Vossi Bop\"; notice the further progression to the genre with Stormzy's Harlem Spartans-like beat and, again, Chief Keef like rap cadence. However, the uniqueness of Stormzy's music is the simpler beats, while still maintaining the drill-styled bass and hi-hat patterns.",
      Artist5Textp1: "Now, this is where we start to see the influence that the United Kingdom drill rap scene has had on music outside of just the UK. Pop Smoke was a New York based rapper who adopted the drill style of music, taking influence from the pioneers mentioned above to create his unique sound. What helped Pop Smoke rise to popularity for his professional and unique sound was from the help of his producer, 808Melo, who was also a producer for many drill rappers based in the United Kingdom. It is interesting to see how the drill rap style of hip-hop made its way from the streets of Chicago, all the way to the United Kingdom where it evolved and gained popularity, only to eventually make its way back to the states and become one of the most popular sub-genres of music today. Here on the left is Pop Smoke's song \"Dior\", which was one of his biggest songs and helped him break out into mainstream music. Notice the similar styles of beats coming from the UK producer 808Melo, and unique tone of voice with a melodic cadence.",
      Artist5Textp2: "As you might know, Pop Smoke was unfortunately killed on February 19th, 2020, from a home invasion that ended with him being shot. May he rest in peace. While he may not be able to make music anymore to further push the style of music further, his legacy will live on forever as an artist that brough the drill style of music back to the states and grew its popularity.",
      Artist6Text: "With Pop Smoke now gone and drill rap being more popular than ever in America, fellow New York rapper, CJ, stands as today's insight into what drill music is and where it is currently going. CJ's song, \"Whoopty\" currently stands as the latest hit drill song, reaching the Billboard top 10 songs throughout the world. Here on the right is CJ's song \"Whoopty\", notice the similar beat and rapping style but unique choice of melody. It will be interesting to see where CJ brings the drill style of music next and see which artists are up next to add their own uniqueness to the music.",

      ConclusionTitle: "In Conclusion",
      ConclusionText: "In conclusion, it is interesting to look at the progression of not only the evolution of the drill style of rap, but the incredible influence that the United Kingdom had on the music. Starting in Chicago, moving all the way to Europe to evolve and gain more popularity, now to travel back to America and grow even more is impressive and exciting to see. While the music is back in America, that does not mean it has left the United Kingdom. The style of music still stands as one of the most popular forms today, with the big artists mentioned above still making music today and contributing to the progression of the sound. It will be interesting to see how the UK and USA will progress. Will they progress together, or will they diverge into their own unique sounds?",

      PersonalStatementPicture: require("@/assets/Pictures/SCU.jpg"),

      PersonalStatementTitle: "What I think",
      PersonalStatementText: "Ever since I first heard this genre of music back in 2012, I always appreciated and enjoyed the unique sounding beats and hard-hitting bass. I never knew of its emergence in the United Kingdom until the research I conducted for this project, and I have really enjoyed what I learned. I appreciated learning of the creative contributions each artist made to the sound, the timeline of it all, and how it traveled all around the world growing in popularity. Even today, I love the direction drill rap is heading and am excited to see what it holds in the future.",
      PersonalStatementText2: "I hope you enjoyed this project and learned a lot about the style of drill music and the culture of the United Kingdom rap scene. I worked very hard on this website, as it is created entirely from scratch by myself, and it took some time. I tried to be as creative as I could with the presentation of information and learned a lot along the way.",
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
