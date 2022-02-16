<template>
  <v-app style="{background: $vuetify.theme.themes.dark.brackround}">
    <sideBar/>
    <sideBarRight/>
    <v-container>
      <v-toolbar color="rgba(0,0,0,0)" flat>
        <v-toolbar-title class="mt-n3">Chosse Category</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-text-field 
          label="Search category or menu..." 
          class="mt-5" color="brown" filled 
          append-icon="mdi-magnify"
          dense solo flat background-color="grey lighten-4"
        />
      </v-toolbar>
      <v-item-group mandatory class="mt-n1">
      <v-container>
        <v-row justify="center">
          <v-col cols="12" md="2">
            <v-item v-slot="{active, toggle}">
              <v-card 
                :color="active ? '#F6EFEF' : 'white' "
                :class="active ? 'borderme' : 'borderout' " 
                class="f-flex align-center rounded-lg mx-2" 
                dark height="140" @click="toggle" flat
              >
                <v-row>
                  <v-col cols="12" sm="12">
                    <v-list-item three-line class="text-center">
                      <v-list-item-content>
                        <div align="center" justify="center">
                          <v-img src="c1.png" max-height="110" max-width="110" contain></v-img>
                        </div>
                        <v-list-item-subtitle :class="active ? 'brown--text' : 'black--text' " class="caption mt-4">
                          All
                        </v-list-item-subtitle>
                      </v-list-item-content>
                    </v-list-item>
                  </v-col>
                </v-row>
              </v-card>
            </v-item>
          </v-col>
          
          <v-col cols="12" md="2">
            <v-item v-slot="{active, toggle}">
              <v-card 
                :color="active ? '#F6EFEF' : 'white' "
                :class="active ? 'borderme' : 'borderout' " 
                class="f-flex align-center rounded-lg mx-2" 
                dark height="140" @click="toggle" flat
              >
                <v-row>
                  <v-col cols="12" sm="12">
                    <v-list-item three-line class="text-center">
                      <v-list-item-content>
                        <div align="center" justify="center">
                          <v-img src="c2.png" max-height="90" max-width="90" contain></v-img>
                        </div>
                        <v-list-item-subtitle :class="active ? 'brown--text' : 'black--text' " class="caption mt-6">
                          Coffee
                        </v-list-item-subtitle>
                      </v-list-item-content>
                    </v-list-item>
                  </v-col>
                </v-row>
              </v-card>
            </v-item>
          </v-col>
          
          <v-col cols="12" md="2">
            <v-item v-slot="{active, toggle}">
              <v-card 
                :color="active ? '#F6EFEF' : 'white' "
                :class="active ? 'borderme' : 'borderout' " 
                class="f-flex align-center rounded-lg mx-2" 
                dark height="140" @click="toggle" flat
              >
                <v-row>
                  <v-col cols="12" sm="12">
                    <v-list-item three-line class="text-center">
                      <v-list-item-content>
                        <div align="center" justify="center">
                          <v-img src="c3.png" max-height="80" max-width="80" contain></v-img>
                        </div>
                        <v-list-item-subtitle :class="active ? 'brown--text' : 'black--text' " class="caption mt-4">
                          Juice
                        </v-list-item-subtitle>
                      </v-list-item-content>
                    </v-list-item>
                  </v-col>
                </v-row>
              </v-card>
            </v-item>
          </v-col>
          
          <v-col cols="12" md="2">
            <v-item v-slot="{active, toggle}">
              <v-card 
                :color="active ? '#F6EFEF' : 'white' "
                :class="active ? 'borderme' : 'borderout' " 
                class="f-flex align-center rounded-lg mx-2" 
                dark height="140" @click="toggle" flat
              >
                <v-row>
                  <v-col cols="12" sm="12">
                    <v-list-item three-line class="text-center">
                      <v-list-item-content>
                        <div align="center" justify="center">
                          <v-img src="c4.png" max-height="80" max-width="80" contain></v-img>
                        </div>
                        <v-list-item-subtitle :class="active ? 'brown--text' : 'black--text' " class="caption mt-4">
                          Millk Based
                        </v-list-item-subtitle>
                      </v-list-item-content>
                    </v-list-item>
                  </v-col>
                </v-row>
              </v-card>
            </v-item>
          </v-col>

          <v-col cols="12" md="2">
            <v-item v-slot="{active, toggle}">
              <v-card 
                :color="active ? '#F6EFEF' : 'white' "
                :class="active ? 'borderme' : 'borderout' " 
                class="f-flex align-center rounded-lg mx-2" 
                dark height="140" @click="toggle" flat
              >
                <v-row>
                  <v-col cols="12" sm="12">
                    <v-list-item three-line class="text-center">
                      <v-list-item-content>
                        <div align="center" justify="center">
                          <v-img src="c5.png" max-height="80" max-width="80" contain></v-img>
                        </div>
                        <v-list-item-subtitle :class="active ? 'brown--text' : 'black--text' " class="caption mt-10">
                          Snack's
                        </v-list-item-subtitle>
                      </v-list-item-content>
                    </v-list-item>
                  </v-col>
                </v-row>
              </v-card>
            </v-item>
          </v-col>

          <v-col cols="12" md="2">
            <v-item v-slot="{active, toggle}">
              <v-card 
                :color="active ? '#F6EFEF' : 'white' "
                :class="active ? 'borderme' : 'borderout' " 
                class="f-flex align-center rounded-lg mx-2" 
                dark height="140" @click="toggle" flat
              >
                <v-row>
                  <v-col cols="12" sm="12">
                    <v-list-item three-line class="text-center">
                      <v-list-item-content>
                        <div align="center" justify="center">
                          <v-img src="c6.png" max-height="80" max-width="80" contain></v-img>
                        </div>
                        <v-list-item-subtitle :class="active ? 'brown--text' : 'black--text' " class="caption mt-10">
                          Dessert
                        </v-list-item-subtitle>
                      </v-list-item-content>
                    </v-list-item>
                  </v-col>
                </v-row>
              </v-card>
            </v-item>
          </v-col>
        </v-row>
      </v-container>
    </v-item-group>
    </v-container>
  </v-app>
</template>

<script>
  import SideBar from '../components/SideBar'
  import SideBarRight from '../components/SideBarRight'

  export default {
    name: 'Home',

    components: {
      SideBar,
      SideBarRight
    }
  }
</script>
<style>
  .v-card-borderme
  {
    border: 2px solid #704232 !important;
  }

  .v-card.borderout
  {
    border: 1px solid #BCAAA4 !important;
  }
</style>