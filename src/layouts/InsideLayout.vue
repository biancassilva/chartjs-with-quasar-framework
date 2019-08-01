<template>
  <q-layout view="lHh Lpr lFf" class="bg-blue-grey-10">
    <q-header elevated>
      <q-toolbar class="bg-blue-grey-9">
        <q-toolbar-title>Chart.js with Quasar Framework</q-toolbar-title>
      </q-toolbar>
    </q-header>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { openURL } from 'quasar'

export default {
  name: 'MyLayout',
  data () {
    return {
      leftDrawerOpen: this.$q.platform.is.desktop
    }
  },
  methods: {
    openURL
  }
}
</script>

<style>
</style>
