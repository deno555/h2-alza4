<template>
  <ion-page>
    <ion-header>
      <ion-toolbar class="toolbar">
        <ion-title class="ion-text-center">Stáže</ion-title>
        <ion-icon color="primary" :icon="icons.personCircleOutline"/>
        <ion-button  color="light" :icon="icons.personCircleOutline"></ion-button>
      </ion-toolbar>
    </ion-header>
    <ion-content>
        <profile />
        <ion-button  @click="addCard()">Test</ion-button>
    </ion-content>
  </ion-page>
</template>
<script>
    import {IonHeader, IonToolbar, IonTitle, IonContent} from '@ionic/vue';
    import Profile from '@/plugins/kokot/component/card.vue';
    import { personCircleOutline, } from 'ionicons/icons'
    export default {
        components: {
            IonHeader, 
            IonToolbar, 
            IonTitle, 
            IonContent,
            Profile,
        },
        data() {
          return {
            icons: {
              personCircleOutline
            }
          }
        }

    }
</script>

<style scoped>

.toolbar{
  height: 80px;
}

.more{
top: 10px;
left: 10px;
}


.filte{
  position: absolute;
}

.filterr{
  position: absolute;
  object-position: right;
}

.ion-text-center{
  font-size: 25px;
  top: 8px;
  }
</style>






