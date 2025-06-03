<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated class="glossy">
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title>
          Timon Dubreuil : Portfolio
        </q-toolbar-title>

        <div>2025</div>
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      style="
      display: flex;
      flex-direction: column;
      "
      width="350"
    >

    <q-timeline layout="dense" style="padding-left: 10px; padding-right: 10px;" class="text-accent" color="accent">
        <NavigationItem
          v-for="link in timelineSections"
          :key="link.title"
          v-bind="link"
        />
      </q-timeline>
      <!-- <q-space></q-space>
      <q-list
        show-if-above
        bordered
        class="text-primary">
      <InfoItem value="+33 7 69 24 14 29" copiedValue="+33769241429" icon="telephone" name="telephone"></InfoItem>
      </q-list> -->
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>

      <q-footer elevated>
        <q-toolbar class="glossy">
          <q-toolbar-title>Footer</q-toolbar-title>
        </q-toolbar>
      </q-footer>
  </q-layout>
</template>

<script>
import NavigationItem from 'components/NavigationItem.vue'

export default {
  name: 'MainLayout',
  components: {
    NavigationItem
  },
  data() {
    return {
      leftDrawerOpen: false,
      timelineSections: [
        {
          title: 'Stage : H2SYS - IHM du système Mothys',
          caption: 'janvier 2025 - mai 2025',
          icon: 'bubble_chart',
          link: '/'
        },
        {
          title: "SAE : S5S6 - boîtier de surveillance qualité de l'eau",
          caption: 'janvier 2025 - mai 2025',
          icon: 'bubble_chart',
          link: '/'
        },
      ],
      infoSections: [
        {
          title:"telephone",
          icon:"telephone",
          value:"+33 7 69 24 14 29",
          copiedValue:"+33769241429"
        }
      ]
    }
  },
  methods: {
    toggleLeftDrawer() {
      this.leftDrawerOpen = !this.leftDrawerOpen
    }
  }
}
</script>
