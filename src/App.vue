<template>
  <v-app>
  <!--<Navbar/> -->  
     
    <Toolbar/>
  
    <v-content>
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script>
//import Navbar from '@/components/Navbar'
import Toolbar from '@/components/Toolbar'
export default {
  name: 'App',

  components: {
    //Navbar,
    Toolbar
  },
  data: () => ({

  }),
};
</script>


