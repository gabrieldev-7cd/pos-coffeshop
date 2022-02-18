<template>
    <v-list-item>
        <v-list-item-avatar rounded color="grey lighten-4">
            <v-img :src="img" />
        </v-list-item-avatar>
        <v-list-item-content>
            <v-list-item-circle class="subtitle-2">{{ title }}</v-list-item-circle>
            <v-list-item-subtitle>{{ 'X' + quant }}
            <v-btn plain color="#704232" small>Notes
                <v-icon right>mdi-pencil</v-icon>
            </v-btn>
            </v-list-item-subtitle>
        </v-list-item-content>
        <v-list-item-action class="caption">${{ value }}</v-list-item-action>
    </v-list-item>
</template>

<script>
export default {
    name: 'ItemBill',

    props:{
        title: String,
        img: String,
        quant: String,
        value: Number
    }
}
</script>