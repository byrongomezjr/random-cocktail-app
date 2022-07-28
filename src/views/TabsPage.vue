<template>

  <ion-page>
    <ion-tabs>
      <ion-router-outlet></ion-router-outlet>
      <ion-tab-bar slot="bottom">

        <!--First Bottom Tab-->
        <ion-tab-button tab="tab1" href="/tabs/tab1">
          <ion-icon :icon="shuffle"></ion-icon>
          <ion-label>Random</ion-label>
        </ion-tab-button>

        <!--Second Bottom Tab-->
        <ion-tab-button tab="tab2" href="/tabs/tab2">
          <ion-icon :icon="flask" />
          <ion-label>Search By Ingredient</ion-label>
        </ion-tab-button>

        <!--Third Bottom Tab-->
        <ion-tab-button tab="tab3" href="/tabs/tab3">
          <ion-icon :icon="square" />
          <ion-label>Tab 3</ion-label>
        </ion-tab-button>
      </ion-tab-bar>
    </ion-tabs>
  </ion-page>

</template>

<script lang="ts">

import { defineComponent } from 'vue';
import { IonTabBar, IonTabButton, IonTabs, IonLabel, IonIcon, IonPage, IonRouterOutlet } from '@ionic/vue';
import { flask, square, shuffle } from 'ionicons/icons';

export default defineComponent({
  name: 'TabsPage',
  components: { IonLabel, IonTabs, IonTabBar, IonTabButton, IonIcon, IonPage, IonRouterOutlet },
  setup() {
    return {
      flask,
      square,
      shuffle,
    }
  }
});

</script>
