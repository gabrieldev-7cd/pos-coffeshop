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
          <v-col cols="12" sm="6" v-for="(sale, i) in SalesItem" :key="i">
            <SalesItem
              :title="sale.title"
              :text="sale.text"
              :img="sale.img"
              :value="sale.value"
            />
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>
  import SideBar from '@/components/SideBar'
  import SideBarRight from '@/components/SideBarRight'
  import CategoryItem from '@/components/CategoryItem'
  import SalesItem from '@/components/SalesItem'

  export default 
  {
    name: 'Home',

    components: 
    {
      SideBar,
      SideBarRight,
      CategoryItem,
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
        ],

        SalesItem:
        [
          {title:"Caramel Frappuccino", text:"Caramel sytrup with coffe, milk and whipped cream.", img:"2.png",value:3.95},
          {title:"Chocolate Frappuccino", text:"Sweet chocolate with coffee, milk, and whipped cream.", img:"3.png", value:4.51}
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