<template>
  <q-layout view="hHh lpR fFf">

    <q-header class="bg-primary text-white">
      <q-toolbar class="header">
        <q-toolbar-title>
            <router-link to="/" class="text-h5 headerFont">DDH</router-link>
        </q-toolbar-title>

      </q-toolbar>
    </q-header>

    <q-drawer v-model="right" side="right" overlay bordered>
      <!-- drawer content -->
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>

  </q-layout>
</template>

<script>
import EssentialLink from 'components/EssentialLink.vue'

export default {
  name: 'MainLayout',
  components: { EssentialLink },
  data () {
    return {
      right: false,
      essentialLinks: linksData
    }
  }
}
</script>

<style lang="scss">
.header {
  height:100px;
  background:rgba(0, 0, 0, 0.4);
}
.headerFont{
  text-decoration: none;
  color:white;
  margin-left:25px;
}

</style>