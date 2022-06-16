<template>          
            <div>
                <a><img src = "https://cdn.discordapp.com/attachments/955521319720599555/969554305457737788/Snimka_obrazovky_2022-04-28_201718.png" /></a>
            </div>
            <div>
                <ContentShow />
            </div>
</template>

<script>
//import header2 from '@/src/plugins/globalComponent/header2.vue';
import ContentShow from '@/plugins/detailPage/component/contentShow.vue'
//import { IonPage, IonContent } from '@ionic/vue';

export default {
    components: { ContentShow} //sem pridat header2 po odkomentovani
}
</script>