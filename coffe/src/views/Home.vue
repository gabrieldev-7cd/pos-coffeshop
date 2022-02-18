<template>
  <v-app :style="{background: $vuetify.theme.themes.dark.background}">
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
            <v-col cols="12" md="2" v-for="(cat, i) in Categories" :key="i">
              <CategoryItem 
                v-bind:title="cat.title" 
                v-bind:image="cat.image" 
                v-bind:width="cat.width" 
                v-bind:height="cat.height" 
                v-bind:space="cat.space"
              />
            </v-col>
          </v-row>
        </v-container>
      </v-item-group>

      <v-toolbar color="#EEEEEE" flat>
        <v-toolbar-title>Coffe Menu</v-toolbar-title>
        <v-spacer/>
        <span color="grey">12 Coffees results</span>
      </v-toolbar>

      <v-row>
        

        <v-col cols="12" sm="6">
          <SalesItem
            title="Caramel Frappuccino"
            text="Caramel sytrup with coffe, milk and whipped cream."
            img="2.png"
            value=3.95
          />

          <v-card flat class="rounded-lg mx-5">
            <v-list-item three-line>
              <v-list-item-avatar rounded size="120" color="grey lighten-4">
                <v-img src="2.png"/>
              </v-list-item-avatar>
              <v-list-item-content>
                <v-list-item-title class="text-h5">
                  Caramel Frappuccino
                </v-list-item-title>
                <v-list-item-subtitle class="mt-1">
                  Caramel sytrup with coffe, milk and whipped cream
                </v-list-item-subtitle>
                <strong class="mt-3">
                  $3.95
                </strong>
              </v-list-item-content>
            </v-list-item>

          <v-card-actions>
            <v-row>
              <v-col cols="12" sm="6" class="mt-1">
                <strong class="ml-3">Mood</strong><br>
                <v-item-group mandatory class="mt-n1">
                  <v-container>
                    <v-row>
                      <!-- Mood's -->
                      <v-col cols="12" md="5">
                        <v-item v-slot="{active, toggle}">
                          <v-card 
                            color="#F6EFEF"
                            :class="active ? 'borderme' : '' "
                            class="d-flex align-center rounded-circle"
                            dark  width="50" height="50" @click="toggle" flat
                          >
                            <v-list-item class="text-center px-2">
                              <v-list-item-content>
                                <v-icon dark color="orange">fas fa-fire</v-icon>
                              </v-list-item-content>
                            </v-list-item>
                          </v-card>
                        </v-item>
                      </v-col>

                      <v-col cols="12" md="6">
                        <v-item v-slot="{active, toggle}">
                          <v-card 
                            color="#F6EFEF"
                            :class="active ? 'borderme' : '' "
                            class="d-flex align-center rounded-circle"
                            dark  width="50" height="50" @click="toggle" flat
                          >
                            <v-list-item class="text-center px-2">
                              <v-list-item-content>
                                <v-icon dark color="blue">fab fa-modx</v-icon>
                              </v-list-item-content>
                            </v-list-item>
                          </v-card>
                        </v-item>
                      </v-col>

                    </v-row>
                  </v-container>
                </v-item-group>
              </v-col>

              <!-- Size's -->
              <v-col cols="12" sm="6" class="mt-1">
                <strong class="ml-2">Size</strong>
                <v-item-group mandatory class="mt-n1">
                  <v-container>
                    <v-row>
                      <v-col cols="12" sm="4">
                        <v-item v-slot="{active, toggle}">
                          <v-card color="#F6EFEF" :class="active ? 'borderme' : '' "
                            class="d-flex align-center rounded-circle"
                            height="50" width="50" @click="toggle" flat
                          >
                            <v-list-item class="text-center">
                              <strong class="font-weight-black">S</strong>
                            </v-list-item>
                          </v-card>
                        </v-item>
                      </v-col>

                      <v-col cols="12" sm="4">
                        <v-item v-slot="{active, toggle}">
                          <v-card color="#F6EFEF" :class="active ? 'borderme' : '' "
                            class="d-flex align-center rounded-circle"
                            height="50" width="50" @click="toggle" flat
                          >
                            <v-list-item class="text-center">
                              <strong class="font-weight-black">M</strong>
                            </v-list-item>
                          </v-card>
                        </v-item>
                      </v-col>

                        <v-col cols="12" sm="4">
                        <v-item v-slot="{active, toggle}">
                          <v-card color="#F6EFEF" :class="active ? 'borderme' : '' "
                            class="d-flex align-center rounded-circle"
                            height="50" width="50" @click="toggle" flat
                          >
                            <v-list-item class="text-center">
                              <strong class="font-weight-black">L</strong>
                            </v-list-item>
                          </v-card>
                        </v-item>
                      </v-col>

                    </v-row>
                  </v-container>
                </v-item-group>

              </v-col>
            </v-row>
          </v-card-actions>

          <v-card-actions>
            <v-row>
              <v-col cols="12" sm="6" class="mt-1">
                <strong class="ml-3">Sugar</strong><br>
                <v-item-group mandatory class="mt-n1">
                  <v-container>
                    <v-row>
                      <!-- Mood's -->
                      <v-col cols="12" md="4">
                        <v-item v-slot="{active, toggle}">
                          <v-card 
                            color="#F6EFEF"
                            :class="active ? 'borderme' : '' "
                            class="d-flex align-center rounded-circle"
                            dark  width="50" height="50" @click="toggle" flat
                          >
                            <v-list-item class="text-center px-2">
                              <v-list-item-content>
                                <strong class="overline" :class="active ? 'brown--text' : 'red--text' ">30%</strong>
                              </v-list-item-content>
                            </v-list-item>
                          </v-card>
                        </v-item>
                      </v-col>

                      <v-col cols="12" md="4">
                        <v-item v-slot="{active, toggle}">
                          <v-card 
                            color="#F6EFEF"
                            :class="active ? 'borderme' : '' "
                            class="d-flex align-center rounded-circle"
                            dark  width="50" height="50" @click="toggle" flat
                          >
                            <v-list-item class="text-center px-2">
                              <v-list-item-content>
                                <strong class="overline" :class="active ? 'brown--text' : 'red--text' ">50%</strong>
                              </v-list-item-content>
                            </v-list-item>
                          </v-card>
                        </v-item>
                      </v-col>

                        <v-col cols="12" md="4">
                        <v-item v-slot="{active, toggle}">
                          <v-card 
                            color="#F6EFEF"
                            :class="active ? 'borderme' : '' "
                            class="d-flex align-center rounded-circle"
                            dark  width="50" height="50" @click="toggle" flat
                          >
                            <v-list-item class="text-center px-2">
                              <v-list-item-content>
                                <strong class="overline" :class="active ? 'brown--text' : 'red--text' ">70%</strong>
                              </v-list-item-content>
                            </v-list-item>
                          </v-card>
                        </v-item>
                      </v-col>

                    </v-row>
                  </v-container>
                </v-item-group>
              </v-col>
              <!-- Size's -->
              <v-col cols="12" sm="6" class="mt-1">
                <strong class="ml-3">Ice</strong>
                <v-item-group mandatory class="mt-n1">
                  <v-container>
                    <v-row>
                      <!-- Mood's -->
                      <v-col cols="12" md="4">
                        <v-item v-slot="{active, toggle}">
                          <v-card 
                            color="#F6EFEF"
                            :class="active ? 'borderme' : '' "
                            class="d-flex align-center rounded-circle"
                            dark  width="50" height="50" @click="toggle" flat
                          >
                            <v-list-item class="text-center px-2">
                              <v-list-item-content>
                                <strong class="overline" :class="active ? 'brown--text' : 'red--text' ">30%</strong>
                              </v-list-item-content>
                            </v-list-item>
                          </v-card>
                        </v-item>
                      </v-col>

                      <v-col cols="12" md="4">
                        <v-item v-slot="{active, toggle}">
                          <v-card 
                            color="#F6EFEF"
                            :class="active ? 'borderme' : '' "
                            class="d-flex align-center rounded-circle"
                            dark  width="50" height="50" @click="toggle" flat
                          >
                            <v-list-item class="text-center px-2">
                              <v-list-item-content>
                                <strong class="overline" :class="active ? 'brown--text' : 'red--text' ">50%</strong>
                              </v-list-item-content>
                            </v-list-item>
                          </v-card>
                        </v-item>
                      </v-col>

                        <v-col cols="12" md="4">
                        <v-item v-slot="{active, toggle}">
                          <v-card 
                            color="#F6EFEF"
                            :class="active ? 'borderme' : '' "
                            class="d-flex align-center rounded-circle"
                            dark  width="50" height="50" @click="toggle" flat
                          >
                            <v-list-item class="text-center px-2">
                              <v-list-item-content>
                                <strong class="overline" :class="active ? 'brown--text' : 'red--text' ">70%</strong>
                              </v-list-item-content>
                            </v-list-item>
                          </v-card>
                        </v-item>
                      </v-col>

                    </v-row>
                  </v-container>
                </v-item-group>
              </v-col>
            </v-row>
          </v-card-actions>


          <v-card-actions>
            <BillButton color="#704232" title="Add Billing"/>
          </v-card-actions>
        </v-card>
      </v-col>


        <v-col cols="12" sm="6">
          <v-card flat class="rounded-lg mx-5">
            <v-list-item three-line>
              <v-list-item-avatar rounded size="120" color="grey lighten-4">
                <v-img src="3.png"/>
              </v-list-item-avatar>
              <v-list-item-content>
                <v-list-item-title class="text-h5">
                  Chocolate Frappuccino
                </v-list-item-title>
                <v-list-item-subtitle class="mt-1">
                  Sweet chocolate with coffee, milk, and whipped cream
                </v-list-item-subtitle>
                <strong class="mt-3">
                  $4.51
                </strong>
              </v-list-item-content>
            </v-list-item>
            <v-card-actions>
              <v-row>
                <v-col cols="12" sm="6" class="mt-1">
                  <strong class="ml-3">Mood</strong><br>
                  <v-item-group mandatory class="mt-n1">
                    <v-container>
                      <v-row>
                        <!-- Mood's -->
                        <v-col cols="12" md="5">
                          <v-item v-slot="{active, toggle}">
                            <v-card 
                              color="#F6EFEF"
                              :class="active ? 'borderme' : '' "
                              class="d-flex align-center rounded-circle"
                              dark  width="50" height="50" @click="toggle" flat
                            >
                              <v-list-item class="text-center px-2">
                                <v-list-item-content>
                                  <v-icon dark color="orange">fas fa-fire</v-icon>
                                </v-list-item-content>
                              </v-list-item>
                            </v-card>
                          </v-item>
                        </v-col>

                        <v-col cols="12" md="6">
                          <v-item v-slot="{active, toggle}">
                            <v-card 
                              color="#F6EFEF"
                              :class="active ? 'borderme' : '' "
                              class="d-flex align-center rounded-circle"
                              dark  width="50" height="50" @click="toggle" flat
                            >
                              <v-list-item class="text-center px-2">
                                <v-list-item-content>
                                  <v-icon dark color="blue">fab fa-modx</v-icon>
                                </v-list-item-content>
                              </v-list-item>
                            </v-card>
                          </v-item>
                        </v-col>

                      </v-row>
                    </v-container>
                  </v-item-group>
                </v-col>

                <!-- Size's -->
                <v-col cols="12" sm="6" class="mt-1">
                  <strong class="ml-2">Size</strong>
                  <v-item-group mandatory class="mt-n1">
                    <v-container>
                      <v-row>
                        <v-col cols="12" sm="4">
                          <v-item v-slot="{active, toggle}">
                            <v-card color="#F6EFEF" :class="active ? 'borderme' : '' "
                              class="d-flex align-center rounded-circle"
                              height="50" width="50" @click="toggle" flat
                            >
                              <v-list-item class="text-center">
                                <strong class="font-weight-black">S</strong>
                              </v-list-item>
                            </v-card>
                          </v-item>
                        </v-col>

                        <v-col cols="12" sm="4">
                          <v-item v-slot="{active, toggle}">
                            <v-card color="#F6EFEF" :class="active ? 'borderme' : '' "
                              class="d-flex align-center rounded-circle"
                              height="50" width="50" @click="toggle" flat
                            >
                             <v-list-item class="text-center">
                                <strong class="font-weight-black">M</strong>
                              </v-list-item>
                            </v-card>
                          </v-item>
                        </v-col>

                         <v-col cols="12" sm="4">
                          <v-item v-slot="{active, toggle}">
                            <v-card color="#F6EFEF" :class="active ? 'borderme' : '' "
                              class="d-flex align-center rounded-circle"
                              height="50" width="50" @click="toggle" flat
                            >
                             <v-list-item class="text-center">
                                <strong class="font-weight-black">L</strong>
                              </v-list-item>
                            </v-card>
                          </v-item>
                        </v-col>

                      </v-row>
                    </v-container>
                 </v-item-group>

                </v-col>
              </v-row>
            </v-card-actions>
            <v-card-actions>
              <v-row>
                <v-col cols="12" sm="6" class="mt-1">
                  <strong class="ml-3">Sugar</strong><br>
                  <v-item-group mandatory class="mt-n1">
                    <v-container>
                      <v-row>
                        <!-- Mood's -->
                        <v-col cols="12" md="4">
                          <v-item v-slot="{active, toggle}">
                            <v-card 
                              color="#F6EFEF"
                              :class="active ? 'borderme' : '' "
                              class="d-flex align-center rounded-circle"
                              dark  width="50" height="50" @click="toggle" flat
                            >
                              <v-list-item class="text-center px-2">
                                <v-list-item-content>
                                  <strong class="overline" :class="active ? 'brown--text' : 'red--text' ">30%</strong>
                                </v-list-item-content>
                              </v-list-item>
                            </v-card>
                          </v-item>
                        </v-col>

                        <v-col cols="12" md="4">
                          <v-item v-slot="{active, toggle}">
                            <v-card 
                              color="#F6EFEF"
                              :class="active ? 'borderme' : '' "
                              class="d-flex align-center rounded-circle"
                              dark  width="50" height="50" @click="toggle" flat
                            >
                              <v-list-item class="text-center px-2">
                                <v-list-item-content>
                                  <strong class="overline" :class="active ? 'brown--text' : 'red--text' ">50%</strong>
                                </v-list-item-content>
                              </v-list-item>
                            </v-card>
                          </v-item>
                        </v-col>

                          <v-col cols="12" md="4">
                          <v-item v-slot="{active, toggle}">
                            <v-card 
                              color="#F6EFEF"
                              :class="active ? 'borderme' : '' "
                              class="d-flex align-center rounded-circle"
                              dark  width="50" height="50" @click="toggle" flat
                            >
                              <v-list-item class="text-center px-2">
                                <v-list-item-content>
                                  <strong class="overline" :class="active ? 'brown--text' : 'red--text' ">70%</strong>
                                </v-list-item-content>
                              </v-list-item>
                            </v-card>
                          </v-item>
                        </v-col>

                      </v-row>
                    </v-container>
                  </v-item-group>
                </v-col>
                <!-- Size's -->
                <v-col cols="12" sm="6" class="mt-1">
                  <strong class="ml-3">Ice</strong>
                  <v-item-group mandatory class="mt-n1">
                    <v-container>
                      <v-row>
                        <!-- Mood's -->
                        <v-col cols="12" md="4">
                          <v-item v-slot="{active, toggle}">
                            <v-card 
                              color="#F6EFEF"
                              :class="active ? 'borderme' : '' "
                              class="d-flex align-center rounded-circle"
                              dark  width="50" height="50" @click="toggle" flat
                            >
                              <v-list-item class="text-center px-2">
                                <v-list-item-content>
                                  <strong class="overline" :class="active ? 'brown--text' : 'red--text' ">30%</strong>
                                </v-list-item-content>
                              </v-list-item>
                            </v-card>
                          </v-item>
                        </v-col>

                        <v-col cols="12" md="4">
                          <v-item v-slot="{active, toggle}">
                            <v-card 
                              color="#F6EFEF"
                              :class="active ? 'borderme' : '' "
                              class="d-flex align-center rounded-circle"
                              dark  width="50" height="50" @click="toggle" flat
                            >
                              <v-list-item class="text-center px-2">
                                <v-list-item-content>
                                  <strong class="overline" :class="active ? 'brown--text' : 'red--text' ">50%</strong>
                                </v-list-item-content>
                              </v-list-item>
                            </v-card>
                          </v-item>
                        </v-col>

                          <v-col cols="12" md="4">
                          <v-item v-slot="{active, toggle}">
                            <v-card 
                              color="#F6EFEF"
                              :class="active ? 'borderme' : '' "
                              class="d-flex align-center rounded-circle"
                              dark  width="50" height="50" @click="toggle" flat
                            >
                              <v-list-item class="text-center px-2">
                                <v-list-item-content>
                                  <strong class="overline" :class="active ? 'brown--text' : 'red--text' ">70%</strong>
                                </v-list-item-content>
                              </v-list-item>
                            </v-card>
                          </v-item>
                        </v-col>

                      </v-row>
                    </v-container>
                  </v-item-group>
                </v-col>
                
              </v-row>
            </v-card-actions>
            <v-card-actions>
              <BillButton color="#704232" title="Add Billing"/>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>
  import SideBar from '../components/SideBar'
  import SideBarRight from '../components/SideBarRight'
  import CategoryItem from '@/components/CategoryItem'
  import SalesItem from '@/components/SalesItem'

  import BillButton from '@/components/BillingButton'

  export default 
  {
    name: 'Home',

    components: 
    {
      SideBar,
      SideBarRight,
      CategoryItem,
      BillButton,
      SalesItem
    },

    data: () => 
    {
      return{
        Categories:
        [
          {title: 'All', image: 'c1.png', width: '110', height: '110', space: 'mt-10'},
          {title: 'Coffee', image: 'c2.png', width: '90', height: '90', space: 'mt-9'},
          {title: 'Juice', image:'c3.png', width: '90', height: '90', space: 'mt-4'},
          {title: 'Milk Based', image:'c4.png', width: '90', height: '90', space: 'mt-4'},
          {title: "Snack's", image:'c5.png', width: '90', height: '90', space: 'mt-11'},
          {title: 'Dessert', image:'c6.png', width: '90', height: '90', space: 'mt-11'}
        ]
      }
    }
  }
</script>
<style>
  .v-card.borderme
  {
    border: 2px solid #704232 !important;
  }

  .v-card.borderout
  {
    border: 1px solid #BCAAA4 !important;
  }
</style>