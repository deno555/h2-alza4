<template>
<ion-page>
  <ion-content>
    <HomePage/>
  </ion-content>
</ion-page>
</template>

<script>
  import HomePage from "@/plugins/kokot/view/homepage.vue"
  import { IonPage, IonContent} from '@ionic/vue';

  export default  {
    components:{
      HomePage,
      IonPage,
      IonContent
    }
  }
</script>