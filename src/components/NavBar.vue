
<template>
  <v-toolbar>
    <v-toolbar-side-icon></v-toolbar-side-icon>
    <v-toolbar-title>{{title}}</v-toolbar-title>
    <v-spacer></v-spacer>
    <v-toolbar-items>
      <v-btn flat
        v-for="(link, idx) in links"
        :key="idx"
        :href="link.href"
      >
        {{link.name}}
      </v-btn>
    </v-toolbar-items>
  </v-toolbar>
</template>

<script>
export default {
  name: 'NavBar',
  props: {
    title: String,
    links: Array,
  },
}
</script>
