<template>
  <v-app>
    <v-content>
      <v-container class="fill-height" fluid>
          <v-row>
            
          </v-row>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  name: 'App',

  components: {
    
  },

  data: () => ({
    step: 1
  }),
  props: {
      source: String
  }
};
</script>