<template>
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
    <v-list suheader two-line class="mt-1">
      <v-list-item>
        <v-list-item-avatar rounded color="grey lighten-4">
          <v-img src="3.png"/>
        </v-list-item-avatar>
        <v-list-item-content>
          <v-list-item-circle class="subtitle-2">Chocolate Frappuccino</v-list-item-circle>
          <v-list-item-subtitle>X1
            <v-btn plain color="#704232" small>Notes
              <v-icon right>mdi-pencil</v-icon>
            </v-btn>
          </v-list-item-subtitle>
        </v-list-item-content>
        <v-list-item-action class="caption">$9.02</v-list-item-action>
      </v-list-item>
    </v-list>
    <v-list suheader two-line class="mt-1">
      <v-list-item>
        <v-list-item-avatar rounded color="grey lighten-4">
          <v-img src="4.png"/>
        </v-list-item-avatar>
        <v-list-item-content>
          <v-list-item-circle class="subtitle-2">Peppermint Macchiato</v-list-item-circle>
          <v-list-item-subtitle>X1
            <v-btn plain color="#704232" small>Notes
              <v-icon right>mdi-pencil</v-icon>
            </v-btn>
          </v-list-item-subtitle>
        </v-list-item-content>
        <v-list-item-action class="caption">$5.34</v-list-item-action>
      </v-list-item>
    </v-list>
    <v-toolbar color="rgba(0,0,0,0)" flat>
      <strong>Subtotal</strong><v-spacer/><strong>$18.31</strong>
    </v-toolbar>
    <v-toolbar color="rgba(0,0,0,0)" flat class="mt-n6">
      <strong>Tax (10%)</strong><v-spacer/><span>$1.83</span>
    </v-toolbar>
      <v-divider class="mx-4"></v-divider>
    <v-toolbar color="rgba(0,0,0,0)" flat>
      <strong>Total</strong><v-spacer></v-spacer><strong>$20.14</strong>
    </v-toolbar>
    <strong class="ml-5">Payment Method</strong>
    <v-item-group mandatory class="mt-1">
      <v-container>
        <v-row justify="center">
          
          <v-col cols="12" md="4" v-for="(item, i) in options" :key="i">
            <PayOption 
              :title="item.title"
              :icon="item.icon"
              :iconColor="item.iconColor"
              :colorActive="item.colorActive"
              :colorCard="item.colorCard"
            />
          </v-col>  

        </v-row>
      </v-container>
    </v-item-group>
    <div class="mx-3 nt-2 mt-2 mb-2">
      <BillButton color="#704232" title="Print Bill"/>
    </div>
  </v-navigation-drawer>
</template>

<script>
  import BillButton from '@/components/BillingButton'
  import PayOption from  '@/components/PayOption'
  export default {
    name: 'SideBarRight',
     components: 
    {
      BillButton,
      PayOption
    },
    data: () => {
      return {
        options:
        [
          {title: 'Cash', icon: 'fas fa-money-bill-wave', iconColor: '#704232', colorActive: 'brown--text', colorCard: '#F6EFEF'},
          {title: 'Debit Card', icon: 'fas fa-credit-card', iconColor: '#704232', colorActive: 'brown--text', colorCard:'#F6EFEF'},
          {title: 'E-Wallet', icon: 'fas fa-qrcode', iconColor: '#704232', colorActive: 'brown--text', colorCard:'#F6EFEF'}
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

  .col-12
  {
    padding: 5px !important;
  }
</style>