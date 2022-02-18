<template>
    <v-item v-slot="{active, toggle}">
        <v-card :color="colorCard" :class=" active ? 'borderme' : '' " class="d-flex align-center rounded-lg" dark height="70" @click="toggle" flat>
            <v-row>
                <v-col cols="12" md="12">
                    <v-list-item three-line class="text-center mt-1">
                        <v-list-item-content>
                            <div>
                                <v-icon :color="active ? iconColor : 'black' ">{{icon}}</v-icon>
                            </div>
                            <v-list-item-subtitle :class="active ? colorActive : 'black--text'" class="mt-n2 caption">{{title}}</v-list-item-subtitle>
                        </v-list-item-content>
                    </v-list-item>
                </v-col>
            </v-row>
        </v-card>
    </v-item>
</template>

<script>
export default {
    name: 'PayOption',
    props:{
        title: String,
        icon: String,
        colorCard: String,
        iconColor: String,
        colorActive: String
    }
}
</script>