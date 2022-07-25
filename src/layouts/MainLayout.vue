<template>
  <q-layout view="lHh Lpr lFf" class="bg-grey-10 text-white">
    <q-header elevated class="bg-grey-5">
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          @click="toggleLeftDrawer"
          aria-label="Menu"
          icon="menu"
        />

        <q-toolbar-title> Meus sites mais usados </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" show-if-above class="bg-grey-9">
      <q-list dark>
        <q-item-label header>Links para Sites</q-item-label>
        <q-item
          clickable
          target="_blank"
          rel="noopener"
          href="https://web.whatsapp.com/"
        >
          <q-item-section avatar>
            <q-icon name="whatsapp" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Whatsapp</q-item-label>
            <q-item-label caption>https://web.whatsapp.com/s</q-item-label>
          </q-item-section>
        </q-item>

        <q-item
          clickable
          target="_blank"
          rel="noopener"
          href="https://github.com/P1nh"
        >
          <q-item-section avatar>
            <q-icon name="code" />
          </q-item-section>
          <q-item-section>
            <q-item-label>GitHub</q-item-label>
            <q-item-label caption>https://github.com/P1nh</q-item-label>
          </q-item-section>
        </q-item>

        <q-item
          clickable
          target="_blank"
          rel="noopener"
          href="https://www.instagram.com/"
        >
          <q-item-section avatar>
            <q-icon name="instagram" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Instagram</q-item-label>
            <q-item-label caption>https://www.instagram.com/</q-item-label>
          </q-item-section>
        </q-item>

        <q-item
          clickable
          target="_blank"
          rel="noopener"
          href="https://cursos.alura.com.br/dashboard"
        >
          <q-item-section avatar>
            <q-icon name="record_voice_over" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Alura</q-item-label>
            <q-item-label caption>https://cursos.alura.com.br</q-item-label>
          </q-item-section>
        </q-item>

        <q-item
          clickable
          target="_blank"
          rel="noopener"
          href="https://twitter.com/home"
        >
          <q-item-section avatar>
            <q-icon name="rss_feed" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Twitter</q-item-label>
            <q-item-label caption>https://twitter.com/home</q-item-label>
          </q-item-section>
        </q-item>
        <q-item
          clickable
          target="_blank"
          rel="noopener"
          href="https://www.facebook.com/arthur.pinheirosilva"
        >
          <q-item-section avatar>
            <q-icon name="public" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Facebook</q-item-label>
            <q-item-label caption>https://www.facebook.com/arthur</q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <div class="Row">
        <div class="col-2"><router-view /></div>
      </div>
    </q-page-container>
  </q-layout>
</template>

<script>
import { ref } from "vue";
export default {
  name: "MyLayout",
  setup() {
    const leftDrawerOpen = ref(false);
    function toggleLeftDrawer() {
      leftDrawerOpen.value = !leftDrawerOpen.value;
    }
    return {
      leftDrawerOpen,
      toggleLeftDrawer,
    };
  },
};
</script>
