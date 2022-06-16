<template>
            <div>
                <h5>Name: {{props.content.Fullname}}</h5>
                <ion-item-divider/>
                <h5>Proffesion: {{props.content.Proffesion}}</h5>
                <ion-item-divider/>
                <h5>Proffesion Language: {{props.content.Proffesion_Language}}</h5>
                <ion-item-divider/>
                <h5>Proffesion Language Level: {{props.content.Proffesion_Language_Level}}</h5>
                <ion-item-divider/>
                <h5>Language: {{props.content.Language}}</h5>
                <ion-item-divider/>
                 <h5>Language Level: {{props.content.Language_Level}}</h5>
                <ion-item-divider/>
                <h5>Pay: {{props.content.Pay}}</h5>
                <ion-item-divider/>
                <h5>Contact Info:</h5>
                <ion-item-divider/>
                <h5>Email: {{props.content.Email}}</h5>
                <ion-item-divider/>
                <h5>Telephoe: {{props.content.Telehone}}</h5>
                <ion-item-divider/>
                <h5>City:{{props.content.City}}</h5>
                <ion-item-divider/>
                <h5>Description: {{props.content.Description}}</h5>
                <ion-item-devider/>
            </div>
</template>
<script>
//import axios from 'axios';
import { IonItemDivider} from '@ionic/vue';


export default {
    components: { IonItemDivider},
    data(){
        return{
            props: {content : [{
                Fullname: [{Name: '', Surname: ''}], Proffesion: '', Proffesion_Language: ['', '', ''], Proffesion_Language_Level: ['', '', ''], Language: '', Language_Level: '', Pay: '', Email: '', Telephone: '', City: '', Description: ''
              }]},
         }
    },

    // computed:{
    //     getList();
    // },

    methods:{
        /*getList(){
            axios.get('http://127.0.0.1:8000/api/v1/').then((response) => { //prepisat url
            response.data;

                this.props[0].content.push({Fullname: response.data.Fullname, Proffesion: response.data.Proffesion, Proffesion_Language: response.data.Proffesion_Language, Proffesion_Language_Level: response.data.Proffesion_Language_Level, Language: response.data.Language, Language_Level: response.data.Language_Level, Pay: response.data.Pay, Email: response.data.Email, Telephone: response.data.Telephone, City: response.data.City, Description: response.data.Description });
            
            }
        )}*/
    }
}


</script>
