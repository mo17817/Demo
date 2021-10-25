<template> 
  <div>
  <div class="q-pa-md">
    <q-layout view="lHh lpr lFf" container style="height: 600px" class="shadow-2 rounded-borders">
      <parralax></parralax>
      <q-header elevated>
         <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
    >
      <q-list>
        <q-item-label
          header
        >
          Essential Links
        </q-item-label>

        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>
        <!-- <q-toolbar class="glossy">
          <q-btn flat round dense icon="menu" class="q-mr-sm" />
          <q-avatar>
            <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg">
          </q-avatar>

          <q-toolbar-title>Quasar Framework</q-toolbar-title>

          <q-btn flat round dense icon="whatshot" />
        </q-toolbar> -->
      </q-header>
      <q-page-container>
        <q-page class="q-pa-md">
          <p v-for="n in 15" :key="n">
           Information after the parralax is here
          </p>
        </q-page>
      </q-page-container>
    </q-layout>
  </div>
  </div>
</template>
<script>
import { defineComponent } from '@vue/composition-api'
import EssentialLink from 'components/EssentialLink.vue'
import MainLayout from 'src/layouts/MainLayout.vue'
import Parralax from 'components/Parralax.vue'

export default defineComponent({
      components: {EssentialLink, Parralax}
})
const linksList = [
  {
    title: 'Docs',
    caption: 'quasar.dev',
    icon: 'school',
    link: 'https://quasar.dev'
  },
  {
    title: 'Github',
    caption: 'github.com/quasarframework',
    icon: 'code',
    link: 'https://github.com/quasarframework'
  },
  {
    title: 'Discord Chat Channel',
    caption: 'chat.quasar.dev',
    icon: 'chat',
    link: 'https://chat.quasar.dev'
  },
  {
    title: 'Forum',
    caption: 'forum.quasar.dev',
    icon: 'record_voice_over',
    link: 'https://forum.quasar.dev'
  },
  {
    title: 'Twitter',
    caption: '@quasarframework',
    icon: 'rss_feed',
    link: 'https://twitter.quasar.dev'
  },
  {
    title: 'Facebook',
    caption: '@QuasarFramework',
    icon: 'public',
    link: 'https://facebook.quasar.dev'
  },
  {
    title: 'Quasar Awesome',
    caption: 'Community Quasar projects',
    icon: 'favorite',
    link: 'https://awesome.quasar.dev'
  }
];
</script>


