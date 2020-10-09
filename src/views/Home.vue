<template>
  <v-app>
    <v-content>
     <v-layout row wrap>
        <v-flex xs12>
          <v-carousel
          cycle
          
          hide-delimiters
          show-arrows-on-hover
          dark
          >
            <v-carousel-item
              v-for="(item,i) in items"
              :key="i"
              :src="item.src"
              class="couleur1"
            >
              <v-row
                class="fill-height"
                align="center"
                justify="space-around"
              >
                <v-container >
                  <div class="d-lg white--text text-sm-center font-weight-bold taille" elevation="9">
                    Bienvenue Mr/Mlle nom_utilisateur <br>
                            SUBLIMONS VOS DONNEES GRACE AU BUSINESS INTELLIGENCE
                  </div>
                  <v-layout row wrap>
                    <v-flex xs12 sm6 class="text-sm-center">
                      <v-btn large router to="/contact" class="red darken-1" elevation="10"> Contactez-Nous ! </v-btn>
                    </v-flex>
                    <v-flex xs12 sm6 class="text-sm-center">
                      <v-btn
                       large
                       router 
                       to="/solution" 
                       class="success" 
                       > 
                        Accedez Aux Solutions 
                      </v-btn>
                    </v-flex>
                  </v-layout>
                </v-container>
              
            </v-row>
            </v-carousel-item>
          </v-carousel>
        </v-flex>
      </v-layout>
      <v-layout row wrap>
        <v-container fluid class="grey lighten-3">
            <h2 class="text-sm-center couleur2"> A propos du site </h2>
            <hr class="separator">
            <p class="text-sm-center font-weight-black">
                Nous présentons ici une brève explication du fonctionnement du site à travers l'extrait vidéo suivante :
            </p>
            <br>
            <br>
            <br>
            <br>
        </v-container>
      </v-layout>
      <v-layout row wrap>
        <v-container fluid class="yellow lighten-2">
            <h2 class="text-sm-center couleur2"> Contactez-Nous! </h2>
            <hr class="separator">
            <p class="text-sm-center font-weight-black">
                      Si vous avez des questions sur le fonctionnement de la solution proposée alors contactez pour plus d'informations
                      en nous laissant un message et nous reviendrons vers vous rapidement.  
            </p> 
            <v-container fluid>
                <v-row align="center" justify="center">
                  <v-col
                    cols="12"
                    sm="6"
                    
                  >
                    <v-form>
                      <v-text-field
                        background-color="grey lighten-2"
                        label="Name"
                        name="Name"
                        type="text"
                        color="success"
                      />
                      <v-text-field
                        background-color="grey lighten-2"
                        label="Email"
                        name="Email"
                        type="text"
                        color="success"
                      />
                      <v-textarea
                          background-color="grey lighten-2"
                          color="success"
                          label="Votre message"
                          rows="5"
                        ></v-textarea>
                    </v-form>
                </v-col>
              </v-row>
          </v-container>
        </v-container>   
      </v-layout>      
    </v-content>
    <v-footer
    dark
    padless
    
    >
    <v-card
      flat
      tile
      class=" white--text text-center mx-auto"  
      width="100%" 
     >
     <v-card-title class="grey darken-4">
     <v-spacer></v-spacer>
     <v-toolbar-items> 
        <v-img src="images/logo_blanc.png" alt="logo des brasseries du Cameroun"></v-img>
      </v-toolbar-items>
        <v-spacer></v-spacer>
        <v-row
        justify="center"
        no-gutters
        >
          <v-btn
              color="white"
              text
              rounded
              class="my-2 mx-12"
          >
            <v-icon small color="white">domain</v-icon>
            Groupe SABC
          </v-btn>
          <v-btn
              color="white"
              text
              rounded
              class="my-2 mx-12"
          >
            <v-icon small color="white">my_location</v-icon>
           77, Rue Prince Bell
          </v-btn>
          <v-btn
              color="white"
              text
              rounded
              class="my-2 mx-12"
          >
            <v-icon small color="white">local_post_office</v-icon>
            BP 4036 Douala Cameroun
          </v-btn>
          <v-btn
              color="white"
              text
              rounded
              class="my-2 mx-12"
          >
            <v-icon small color="white">phone</v-icon>
            00 237 233 42 91 33
          </v-btn>
        </v-row>
      </v-card-title>
      <v-card-text class="white--text">
        Copyright (c) 2020 Sabc-Douala, Tout Droit Réservé. 
      </v-card-text>
    </v-card>
  </v-footer>
  </v-app>
</template>

<script>
export default {
   data () {
      return {
        items: [
          {
            src: 'images/caro1.jpg',
          },
          {
            src: 'images/caro2.jpg',
          },
          {
            src: 'images/caro3.jpg',
          },
        ],
      }
    },
  }
</script>

<style scoped>
.taille
{
  font-size: 40px;
  opacity: 0.9;
  text-shadow: 10px 16px 10px black; /* ombre */
}
.separator 
{
    height: 3px;
    width: 5%;
    border: none;
    box-shadow: none;
    background-color: #fb2c43;
    margin-left: 48%;
    margin-top: 1%;
    margin-bottom: 1%;
}
.couleur1
{
  filter: brightness(0.8);
}

.couleur2
{
  color: #fb2c43;
}
</style>