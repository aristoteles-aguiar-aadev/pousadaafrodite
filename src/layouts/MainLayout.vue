<template>
  <q-layout view="lHh Lpr lFf">
    <q-header class="bg-grey-3 text-grey-9">
      <q-toolbar style="background:#EEEEEE ">


        <q-toolbar-title style="margin:20px" class="text-center">
          <div class="text-h2" style="font-family: 'Poppins', sans-serif; color:orange">Pousada Afrodite</div>
        </q-toolbar-title>

      </q-toolbar>
    </q-header>

    <q-drawer v-model="drawer" show-if-above width="220" bordered breakpoint-up="30" class="bg-grey-3 text-grey-7"
      width:200px>
      <img style="width: 120px; margin: 10px 0 0 50px;" src="../assets/img/pousada-afrodite-2.png" alt="" srcset="">


      <q-list>
        <q-item-label header>

          <div style="margin-left:55px">Bem Vindo!</div>

          <q-separator class="q-mb-md" />
        </q-item-label>
        <q-space></q-space>
        <EssentialLink v-for="link in essentialLinks" :key="link.title" v-bind="link" />
      </q-list>

    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'
import EssentialLink from 'components/EssentialLink.vue'
import { list } from 'postcss'

const linksList = [
  {
    title: 'Home',
    caption: 'inicio',
    link: 'https://pousadaafrodite.com.br'
  },
  {
    title: 'Acomodações',
    caption: 'Ambiente',
    link: 'https://pousadaafrodite.com.br/pousada'
  },
  {
    title: 'Serviços',
    caption: 'Bar / Loja',
    link: 'https://pousadaafrodite.com.br/pousada'
  },



]

export default defineComponent({
  name: 'MainLayout',

  components: {
    EssentialLink
  },

  setup() {
    const leftDrawerOpen = ref(false)

    return {
      essentialLinks: linksList,
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
})
</script>
