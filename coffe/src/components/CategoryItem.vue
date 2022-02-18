<template>
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
                    <v-img v-bind:src="image" v-bind:max-height="height" v-bind:max-width="width" contain></v-img>
                    </div>
                    <v-list-item-subtitle :class="[ active ? 'brown--text' : 'black--text', space]" class="caption">
                    {{ title }}
                    </v-list-item-subtitle>
                </v-list-item-content>
                </v-list-item>
            </v-col>
            </v-row>
        </v-card>
    </v-item>
</template>

<script>
// c1.png
export default (
    {
        name: 'CategoryItem',
        
        props:
        {
            title: String,
            image: String,
            width: String,
            height: String,
            space: String
        }
    }
)
</script>