<template>
  <v-navigation-drawer app color="white" right width="290">
    <v-list subheader two-line class="mt-1">
      <v-list-item>
        <v-list-item-avatar rounded>
          <v-img src="https://cdn.vuetifyjs.com/images/lists/2.jpg"/>
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
    <v-list suheader two-line class="mt-1" v-for="(item, i) in itens" :key="i">
      <ItemBill 
        :title="item.title"
        :img="item.img"
        :quant="item.quant"
        :value= item.value
      />
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
  import ItemBill from '@/components/ItemBill'

  export default {
    name: 'SideBarRight',
     components: 
    {
      BillButton,
      PayOption,
      ItemBill
    },
    data: () => {
      return {
        options:
        [
          {title: 'Cash', icon: 'fas fa-money-bill-wave', iconColor: '#704232', colorActive: 'brown--text', colorCard: '#F6EFEF'},
          {title: 'Debit Card', icon: 'fas fa-credit-card', iconColor: '#704232', colorActive: 'brown--text', colorCard:'#F6EFEF'},
          {title: 'E-Wallet', icon: 'fas fa-qrcode', iconColor: '#704232', colorActive: 'brown--text', colorCard:'#F6EFEF'}
        ],
        itens:
        [
          {title: 'Caramel Frappuccino', img: '2.png', quant: 1, value: 3.95},
          {title: 'Chocolate Frappuccino', img: '3.png', quant: 1, value: 9.02},
          {title: 'Peppermint Macchiato', img: '4.png', quant: 1, value: 5.34}
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