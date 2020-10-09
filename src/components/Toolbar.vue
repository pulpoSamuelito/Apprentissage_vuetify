<template >
    <v-toolbar height="100px" color="#ffcc01" tile outlined>
        <v-spacer></v-spacer>
        <v-toolbar-items> 
            <v-img  src="images/logo_sabc.jpg" alt="logo des brasseries du Cameroun"></v-img>
        </v-toolbar-items>
         <v-spacer></v-spacer>
        <v-row
        justify="center"
        no-gutters
        >
         <v-btn
            color="black"
            text
            rounded
            class="my-2 mx-5" 
            href="/"
        >
           <v-icon small color="black">fas fa-home</v-icon>
           Acceuil
        </v-btn>
        <v-btn
            color="black"
            text
            rounded
            class="my-2 mx-10"
            href="/apropos"
        >
           <v-icon small color="black">fas fa-comment-dots</v-icon>
           A propos
        </v-btn>
        <v-btn
            color="black"
            text
            rounded
            class="my-2 mx-5"
            href="/contact"
        >
           <v-icon small color="black">fas fa-id-card</v-icon>
           Contact
        </v-btn>
        </v-row>
        <v-spacer></v-spacer>
         <v-row
        justify="center"
        no-gutters
        >
        <v-btn
            color="black"
            text
            rounded
            class="my-2"
            
        >
           <v-icon small color="black">fas fa-user</v-icon>
           Nom_utilisateur
        </v-btn>
         <v-btn
            color="black"
            text
            rounded
            class="my-2"
            href="/deconnexion"
        >
           <v-icon small color="black">fas fa-sign-out-alt</v-icon>
           Se Déconnecter
        </v-btn>
         </v-row>
      
    </v-toolbar>
</template>

<script>
export default {
    data: () => ({
             
    })
}
</script>

<style scoped>

</style>