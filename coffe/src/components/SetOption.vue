<template>
   <v-col cols="12" sm="6" class="mt-1">
    <strong class="ml-3">{{ title }}</strong><br>
    <v-item-group mandatory class="mt-n1">
      <v-container>
        <v-row>
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
</template>

<script>
export default {
    name: 'SetOption',
    
    props:{
        title: String,
        itens: Object
    }
}
</script>