<template>
    <v-list-item three-line>
        <v-list-item-avatar rounded size="120" color="grey lighten-4">
            <v-img :src="img"/>
        </v-list-item-avatar>
        <v-list-item-content>
            <v-list-item-title class="text-h5">
                {{ title }}
            </v-list-item-title>
        <v-list-item-subtitle class="mt-1">
            {{ text }}
        </v-list-item-subtitle>
        <strong class="mt-3">
            {{'$'+value}}
        </strong>
        </v-list-item-content>
    </v-list-item>
</template>

<script>
export default {
    name: 'DisplayItem',
    props:{
        title: String,
        text: String,
        img: String,
        value: Number
    }
}
</script>
