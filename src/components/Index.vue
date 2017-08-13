<template>
  <q-layout>
    <div slot="header" class="toolbar">
      <button class="hide-on-drawer-visible" @click="$refs.drawer.open()">
        <i>menu</i>
      </button>
      <q-toolbar-title :padding="1">
        {{pageTitle}}
      </q-toolbar-title>
    </div>

    <q-drawer ref="drawer">
      <div class="toolbar">
        <button class="hide-on-drawer-visible" @click="$refs.drawer.close()">
          <i>menu</i>
        </button>
        <q-toolbar-title :padding="1">
          Menu
        </q-toolbar-title>
      </div>
      <div class="list no-border platform-delimiter">
        <q-drawer-link icon="dashboard" to="/dashboard">
          Dashboard
        </q-drawer-link>
        <q-drawer-link icon="assessment" to="/stocks">
          Stocks
        </q-drawer-link>
        <q-drawer-link icon="attach_money" to="/expenses">
          Expenses
        </q-drawer-link>
        <q-drawer-link icon="accessibility" to="/activities">
          Activities
        </q-drawer-link>
        <q-drawer-link icon="compare_arrows" to="/utilities">
          Utilities
        </q-drawer-link>
      </div>
    </q-drawer>

    <router-view ref="currentPage" class="layout-view"></router-view>

  </q-layout>
</template>

<script>
export default {
  data () {
    return {
      pageTitle: 'The Karma Tracker'
    }
  },
  mounted () {

  }
}
</script>
