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
            
            <v-col cols="12" sm="6" class="mt-1" v-for="(obj, i) in objects" :key="i" >
                <SetOption
                    :isIcon="obj.isIcon"
                    :itens="obj"
                />
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
    },

    data: () => {
        return {
            objects:
            [   
                { title: "Mood", isIcon: true, options: [{color: 'orange', icon: 'fas fa-fire'},{color: 'blue', icon: 'fab fa-modx'}]},
                { title: "Size", isIcon: false, options: ['S', 'M','L']},
                { title: "Sugar", isIcon: false, options: ['30%', '50%','70%']},
                { title: "Ice", isIcon: false, options: ['30%', '50%','70%']}
            ]
        }
    }
}
</script>

<style>

</style>