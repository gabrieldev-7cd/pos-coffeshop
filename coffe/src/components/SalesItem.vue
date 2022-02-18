<template>
 <v-card flat class="rounded-lg mx-5">
            

          <v-card-actions>
             
            <v-row>
                <DisplayItem 
                    :title="title"
                    :text="text"
                    :img="img"
                    :value="value"
                />


             <SetOption />

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
  
</template>

<script>
    import BillButton from '@/components/BillingButton'
    import SetOption from '@/components/SetOption'
    import DisplayItem from  '@/components/DisplayItem'
export default {
    name: 'SalesItem',

    components:
    {
      BillButton,
      SetOption,
      DisplayItem
    },
    props:{
        title: String,
        text: String,
        img: String,
        value: Number,
        // options: Object
    }
}
</script>

<style>

</style>