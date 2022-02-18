<template>

    <v-item-group mandatory class="mt-n1">
    <strong class="ml-3">{{ itens.title }}</strong><br>
      <v-container>
        <v-row>
          <v-col cols="12" md="4" v-for=" (item, i) in itens.options" :key="i">
            <v-item v-slot="{active, toggle}">
              <v-card 
                color="#F6EFEF"
                :class="active ? 'borderme' : '' "
                class="d-flex align-center rounded-circle"
                dark  width="50" height="50" @click="toggle" flat
              >
                <v-list-item class="text-center px-2">
                  <v-list-item-content>
                    <v-icon v-show="isIcon" dark :color="itens.options[i].color">{{ itens.options[i].icon }}</v-icon>
                    <strong v-show="!isIcon" :class="active ? 'brown--text' : 'black--text' ">{{ itens.options[i] }}</strong>
                  </v-list-item-content>
                </v-list-item>
              </v-card>
            </v-item>
          </v-col>

        </v-row>
      </v-container>
    </v-item-group>

</template>

<script>
export default {
    name: 'SetOption',
    
    props:{
        isIcon: Boolean,
        itens: Object
    }
}
</script>