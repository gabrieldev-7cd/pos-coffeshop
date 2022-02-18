<template>
  <v-btn :color="color" block dark class="widthoutuppercase mb-2">{{title}}</v-btn>
</template>

<script>
export default {
    name: 'OptionButton',
    props:{
        color: String,
        title: String
    }
}
</script>