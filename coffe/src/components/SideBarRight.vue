<template>
  <div>
    <v-navigation-drawer app color="white" right width="290">
      <v-list subheader two-line class="mt-1">
        <v-list-item>
          <v-list-item-avatar rounded>
            <v-img src="https://cdn.vuetifyjs.com/images/lists/2.jpg" />
          </v-list-item-avatar>
          <v-list-item-content>
            <v-list-item-subtitle>I'm a Cashier</v-list-item-subtitle>
            <v-list-item-title>Jelly Grande</v-list-item-title>
          </v-list-item-content>
          <v-list-item-action>
            <v-badge bordered overlap color="red" dot>
              <v-icon>far fa-bell</v-icon>
            </v-badge>
          </v-list-item-action>
        </v-list-item>
      </v-list>
      <strong class="ml-3">Bills</strong>
      <v-list suheader two-line class="mt-1">
        <v-list-item>
          <v-list-item-avatar rounded color="grey lighten-4">
            <v-img src="2.png"/>
          </v-list-item-avatar>
          <v-list-item-content>
            <v-list-item-circle class="subtitle-2">Caramel Frappuccino</v-list-item-circle>
            <v-list-item-subtitle>X1
              <v-btn plain color="#704232" small>Notes
                <v-icon right>mdi-pencil</v-icon>
              </v-btn>
            </v-list-item-subtitle>
          </v-list-item-content>
          <v-list-item-action class="caption">$3.95</v-list-item-action>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {

}
</script>

<style>
  .v-card.boarderme
  {
    border: 2px solid #704232 !important;
  }

  .col-12
  {
    padding: 5px !important;
  }

  .v-btn.widthoutuppercase
  {
    text-transform: none !important;
  }

</style>