<template>
  <ion-page>
    <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Stazista</ion-title>
        </ion-toolbar>
      </ion-header>
    <ion-content :fullscreen="true">  
      
      <AADetailsPage />
      
      </ion-content>
  </ion-page>
</template>

<script lang="ts">
import AADetailsPage from '@/plugins/detailPage/view/AADetailsPage.vue';
import { IonPage, IonContent, IonHeader, IonToolbar, IonTitle,} from '@ionic/vue';
  // import AHeader \import header2 from '@/plugins/global_component/AHeader.vue'\ 

  export default{
      components: {AADetailsPage, IonPage, IonContent, IonHeader, IonToolbar, IonTitle,} // pridat 'AHeader'
  }
</script> 