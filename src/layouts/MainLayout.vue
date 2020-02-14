<template>
  <q-layout view="hHh lpR fFf">

    <q-header bordered class="bg-primary text-white" height-hint="98">
      <q-toolbar>
        <q-toolbar-title>
          <q-btn flat label="MARIA BOGOMAZ" size="xl" :ripple="{ center: true }"/>
        </q-toolbar-title>
        <q-tabs>
          <q-tab label="Portfolio" @click="scrollTo('portfolio')" :ripple="{ center: true }" />
          <q-tab label="Resume" @click="scrollTo('resume')" :ripple="{ center: true }" />
          <q-tab label="About" @click="scrollTo('about')" :ripple="{ center: true }" />
          <q-tab label="Contact" @click="scrollTo('contact')" :ripple="{ center: true }" />
        </q-tabs>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>

  </q-layout>
</template>

<script>
export default {
  name: 'MainLayout',

  components: {
  },

  data () {
    return {
      leftDrawerOpen: false
    }
  },

  methods: {
    scrollTo (id) {
      document.getElementById(id).scrollIntoView({ block: 'end', behavior: 'smooth' })
    }
  }
}
</script>
