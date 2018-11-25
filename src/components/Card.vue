<template>
  <v-card>
    <v-img
      :src="data.image"
      aspect-ratio="1.5"
    ></v-img>

    <v-card-title primary-title>
      <div>
        <h3 class="headline mb-0">{{data.name}}</h3>
        <div>{{data.info}}</div>
      </div>
    </v-card-title>

    <v-card-actions>
      <v-btn flat color="orange">Share</v-btn>
      <v-btn flat color="orange">Explore</v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  name: 'Card',
  props: {
    data: Object,
  },
}
</script>
