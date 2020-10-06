<template>
  <v-app :style="{background: $vuetify.theme.themes.light.background}">
    <v-container>
      <v-layout row class="ma-4">
        <v-app style="background-color: grey lighten-1;" class="rounded">
          <v-row>
            <v-col cols="12" md="8" class="ligne">
              <v-container>
                <v-row>
                  <v-col cols="12" md="9" offset-md="1">
                    <v-text-field label="Search" prepend-inner-icon="search"></v-text-field> 
                  </v-col>
                  <v-col cols="12" md="2" align="center" justify="center">
                    <v-badge color="error" overlap class="mt-5">
                      <template v-slot:badge> 2 </template> 
                      <v-icon color="tertiary">mdi-bell</v-icon> 
                    </v-badge> 
                  </v-col> 
                  <v-col cols="12" md="9">
                    <h1 class="headline mb-2 grey--text">Money Status</h1>
                    <template>
                      <div class="dashboard">
                        <GChart
                        type="ColumnChart"
                        :data="chartData"
                        :options="chartOptions"/>
                      </div>
                    </template>
                  </v-col>
                  <v-col cols="12" md="12"><h1 class="headline mb-2 grey--text">Budgets</h1></v-col>
                  <v-col cols="12" md="8">
                    <v-card>
                      <v-list>
                        <v-list-item>
                          <v-list-item-avatar color="blue">
                            <v-icon dark>fas fa-car</v-icon>
                          </v-list-item-avatar>
                          <v-list-item-content>
                            <v-list-item-title> Auto & transport</v-list-item-title>
                            <v-list-item-subtitle>$700 left</v-list-item-subtitle>
                          </v-list-item-content>
                          <v-list-item-content align="right">
                            <v-list-item-title class="indigo--text">$1.200</v-list-item-title>
                            <v-list-item-subtitle>$500 of 1.200</v-list-item-subtitle>
                          </v-list-item-content>
                        </v-list-item>
                        <v-divider inset></v-divider>
                        <v-list-item>
                          <v-list-item-avatar color="red">
                            <v-icon dark>fas fa-utensils</v-icon>
                          </v-list-item-avatar>
                          <v-list-item-content>
                            <v-list-item-title> Food & Drink </v-list-item-title>
                            <v-list-item-subtitle>$2.70 left</v-list-item-subtitle>
                          </v-list-item-content>
                          <v-list-item-content align="right">
                            <v-list-item-title class="indigo--text">$3.200</v-list-item-title>
                            <v-list-item-subtitle>$900 of 3.200</v-list-item-subtitle>
                          </v-list-item-content>
                        </v-list-item>
                      </v-list>
                    </v-card>  
                  </v-col>
                  <v-col cols="12" md="4">
                    <v-card class="mx-auto" max-height="400">
                      <v-img class="white--text align-end" height="150px" src="110.jpg"></v-img>
                      <v-card-title class="pb-0">Cash loan</v-card-title>
                      <v-card-text class="text-primary">
                        <div>Up to 2 million dollards</div>
                        <div>Money the next date. Rate</div>
                      </v-card-text>
                    </v-card>
                  </v-col>
                </v-row>
              </v-container>
            </v-col>
            <v-col cols="12" md="4">
              <v-container>
                <v-row>
                  <v-col cols="12" md="12">
                    <v-list-item>
                      <v-list-item-avatar>
                        <v-img src="2790917.jpg"></v-img>
                      </v-list-item-avatar>
                      <v-list-item-content>
                        <v-list-item-title>AAE IdePro</v-list-item-title>
                        <v-list-item-subtitle>aaeideapro@gmail.com</v-list-item-subtitle>
                      </v-list-item-content>
                      <v-list-item-action>
                        <v-icon>fas fa-sign-out-alt</v-icon>
                      </v-list-item-action>
                    </v-list-item>
                    <v-divider inset></v-divider>
                  </v-col>

                  <v-col cols="12" md="12">
                    <v-list-item>
                      <v-list-item-avatar color="grey">
                        <v-icon color="white">fas fa-dollar-sign</v-icon>
                      </v-list-item-avatar>
                      <v-list-item-content>
                        <v-list-item-title> Heisenberg </v-list-item-title>
                        <v-list-item-subtitle>$ 15.245</v-list-item-subtitle>
                      </v-list-item-content>
                      <v-list-item-action>
                        <v-icon color="indigo" large>fab fa-cc-visa</v-icon>
                      </v-list-item-action>
                    </v-list-item>
                  </v-col>
                  <v-col cols="12" md="12">
                    <v-card color="#952175" dark>
                      <div class="d-flex flex-no-wrap justify-space-between">
                        <div>
                          <v-card-title class="headline"> Upgrade to your plan gold</v-card-title>
                          <v-card-subtitle> With Gold account plan you get to premium feature</v-card-subtitle>
                        </div>
                        <v-avatar class="ma-3" size="100" tile>
                          <v-img src="4350636.jpg"></v-img>
                        </v-avatar>
                      </div>
                    </v-card>
                  </v-col>
                </v-row>
              </v-container>  
            </v-col> 
          </v-row>
        </v-app>
      </v-layout>
    </v-container>
  </v-app>
</template>

<script>
 // import from '@/components.vue';
  
  export default {
    name: "dashboard",
    components: {
    
    },
    computed: {
      theme(){
        return (this.$vuetify.theme.dark) ? 'dark' : 'light'
      }
    },
    data: () => ({
      chartData: [
        ["Year", "Sales", "Expenses", "Profit"],
        ["2014", 1000, 400, 200],
        ["2015", 1100, 450, 250],
        ["2016", 600, 1400, 300],
        ["2017", 1040, 500, 350],
        ["2018", 1800, 590, 400],
        ["2019", 1080, 700, 450],
      ],
      chartOptions: {
        chart: {
          title: "Company Performance",
          subtitle: "Sales, Expenses, and Profit: 2016-2019"
        }
      }
  })
  }
</script>

<style scoped>
.rounded
{
    border-radius: 30px;
}
.ligne
{
  border-right: 1px solid #2c3e50;
}
</style>