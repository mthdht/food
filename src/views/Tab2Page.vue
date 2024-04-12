<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Tab 2</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 2</ion-title>
        </ion-toolbar>
      </ion-header>

      <div id="map" class="h-full"></div>
    </ion-content>
  </ion-page>
</template>

<script setup>
import { onMounted } from 'vue';
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent } from '@ionic/vue';

import "leaflet/dist/leaflet.css";

import L from 'leaflet'

onMounted(() =>{
  var map = L.map('map').setView([51.505, -0.09], 13);
  console.log(map)
})
</script>

<style scoped>
#map {
  height: 100%
}
</style>