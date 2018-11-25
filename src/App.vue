<template>
  <v-app>
    <NavBar :title="navTitle" :links="navLinks" />
    <v-layout row justify-center>
      <v-flex xs4>
        <Card :data="cities[0]" />
      </v-flex>
      <v-flex xs4>
        <Card :data="cities[1]" />
      </v-flex>
      <v-flex xs4>
        <Card :data="cities[2]" />
      </v-flex>
    </v-layout>
    <Footer />
  </v-app>
</template>

<script>
import NavBar from '@/components/NavBar'
import Card from '@/components/Card'
import Footer from '@/components/Footer'

export default {
  name: 'App',
  components: {
    NavBar,
    Card,
    Footer,
  },
  data: () => ({
    navTitle: 'F2E Good',
    navLinks: [
      {
        name: 'Angular',
        href: 'https://angular.io',
      },
      {
        name: 'React',
        href: 'https://reactjs.org',
      },
      {
        name: 'Vue',
        href: 'https://vuejs.org',
      },
    ],
    cities: [
      {
        name: 'Paris',
        image: 'https://www.w3schools.com/bootstrap4/paris.jpg',
        info: 'Paris is the capital and most populous city of France, with an area of 105 square kilometres and a population of 2,206,488.',
      },
      {
        name: 'New York',
        image: 'https://www.w3schools.com/bootstrap4/newyork.jpg',
        info: 'New York City is the most populous city in the United States. With an estimated 2017 population of 8,622,698 distributed over a land area of about 302.6 square miles.',
      },
      {
        name: 'San Francisco',
        image: 'https://www.w3schools.com/bootstrap4/sanfran.jpg',
        info: 'San Francisco, officially the City and County of San Francisco, is the cultural, commercial, and financial center of Northern California.',
      },
    ]
  }),
}
</script>

<style>
.layout {
  margin: 0 1em;
}
.v-card {
  margin: 1em;
}
</style>
