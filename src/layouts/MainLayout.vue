<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn flat dense round icon="menu" aria-label="Menu" @click="toggleLeftDrawer" />

        <q-toolbar-title>
          Timon Dubreuil : Portfolio
        </q-toolbar-title>

        <div>2025</div>
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" bordered style="
      display: flex;
      flex-direction: column;
      " width="350">


      <q-timeline layout="dense" style="padding-left: 10px; padding-right: 10px;" class="text-primary" color="primary">
        <NavigationItem v-for="link in timelineSections" :key="link.title" v-bind="link"
          @navigate="navigate(link.target_id)" />
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
      <q-toolbar>
        <div class="row">
          <InfoItem v-for="item in infoSections" :key="item.title" :title="item.title" :value="item.value"
            :copiedValue="item.copiedValue" :icon="item.icon" :name="item.name">
          </InfoItem>
        </div>
      </q-toolbar>
    </q-footer>
  </q-layout>
</template>

<script>
import NavigationItem from 'components/NavigationItem.vue'
import InfoItem from 'components/InfoItem.vue';

export default {
  name: 'MainLayout',
  components: {
    NavigationItem,
    InfoItem
  },
  data() {
    return {
      leftDrawerOpen: false,
      timelineSections: [
        {
          title: "Présentation de l'entreprise",
          // icon: 'bubble_chart',
          target_id: 'heading_1'
        },
        {
          title: "Sujet du stage",
          target_id: 'heading_2'
        },
        {
          title: "Technologies utilisées",
          target_id: 'heading_3'
        },
        {
          title: "Rôle et fonctionnalités de l'IHM",
          target_id: 'heading_4'
        },
        {
          title: "Réalisation",
          target_id: 'heading_5'
        },
        {
          title: "Compétences mobilisées",
          target_id: 'heading_6'
        },
        {
          title: "Bilan",
          target_id: 'heading_7'
        },
        // {
        //   title: "SAE : S5S6 - boîtier de surveillance qualité de l'eau",
        //   caption: 'janvier 2025 - mai 2025',
        //   icon: 'bubble_chart',
        //   link: '/'
        // },
      ],
      infoSections: [
        {
          title: "telephone",
          icon: "phone",
          value: "+33 7 69 24 14 29",
          copiedValue: "+33769241429",
          name: "numéro de téléphone"
        },
        {
          title: "email",
          icon: "email",
          value: "timondubreuil@outlook.com",
          copiedValue: "timondubreuil@outlook.com",
          name: "addresse email"
        },
        {
          title: "github",
          icon: "fa-brands fa-github",
          value: "https://github.com/Dandjix",
          copiedValue: "https://github.com/Dandjix",
          name: "github"
        }
      ]
    }
  },
  methods: {
    toggleLeftDrawer() {
      this.leftDrawerOpen = !this.leftDrawerOpen
    },
    navigate(id) {
      const el = document.getElementById(id);
      if (el) {
        const offset = 100;
        const y = el.getBoundingClientRect().top + window.pageYOffset - offset;

        window.scrollTo({
          top: y,
          behavior: 'smooth'
        });
      }
    }

  }
}
</script>
