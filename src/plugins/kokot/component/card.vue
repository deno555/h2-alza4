<template>
    <div v-for="(i) in card" :key="i.cardTitle" class="userCard">
      <ion-card @click="redirect()">
        <ion-card-header>
            <div class="images">
            <img class="img1" src="https://www.business2community.com/wp-content/uploads/2017/08/blank-profile-picture-973460_640.png">
            </div>
        </ion-card-header>

        <ion-card-content>
            <p v-for="j in lessThanID(cardAll)" v-bind:key="j.cardName" >{{j.names}}</p>
            <p v-for="j in lessThanID(cardAll)" v-bind:key="j.cardJob" >{{j.jobs}}</p>
            <p v-for="j in lessThanID(cardAll)" v-bind:key="j.cardSkill" >{{j.skills}}</p>
            <p v-for="j in lessThanID(cardAll)" v-bind:key="j.cardMoney" >{{j.moneys}}</p>
            <p v-for="j in lessThanID(cardAll)" v-bind:key="j.cardCity" >{{j.citys}}</p>
        </ion-card-content>
      </ion-card>
  </div>
</template>



<script>
    export default{
        data(){
            return{
                //veci ktore zoberem z backendu
                name:'',
                job:'',
                jobSkills:'',
                money:'',
                city:'',
                img:document.getElementById("imgs"),
                //veci ktore vytvorim tu
                counter:1,
                card:[
                    {cardID:1},
                    {cardID:2},
                    {cardID:3},
                    {cardID:4},
                    {cardID:5},
                    {cardID:6},
                ],

                cardAll:[
                    {names:"Madison Rao", jobs:"Programmer",skills:"Python", moneys:"21€",citys:"Bratislava",cardID:"1"},
                    {names:"Kirils Waterman", jobs:"Electrician",skills:"", moneys:"22€",citys:"London",cardID:"2"},
                    {names:"Matthieu Hollins", jobs:"Teacher",skills:"", moneys:"23€",citys:"Washington",cardID:"3"},
                    {names:"Alexandros Daniel", jobs:"Janitor",skills:"", moneys:"24€",citys:"Tokyo",cardID:"4"},
                    {names:"Vladimir Johns", jobs:"Doctor",skills:"", moneys:"25€",citys:"Brighton",cardID:"5"},
                    {names:"Yaropolk Aakster", jobs:"Programmer",skills:"Javascript", moneys:"26€",citys:"Košice",cardID:"6"},
                ]
            }
        },
            
        methods:{
            addCard(cardID){
                this.idCount++
                this.card.push({
                    cardID:cardID+1,
                })
            },

            addName(cardID){
                this.cardName.push({
                    names:this.name,
                    cardID:cardID+1
                }),
                this.name=''
            },

            addJob(cardID){
                this.cardJob.push({
                    jobs:this.job,
                    cardID:cardID+1
                }),
                this.job=''
            },
            
            addSkill(cardID){
                this.cardSkill.push({
                    skills:this.jobSkills,
                    cardID:cardID+1
                }),
                this.jobSkills=''  
            },

            addMoney(cardID){
                this.cardMoney.push({
                    moneys:this.money,
                    cardID:cardID+1
                }),
                this.money=''
            },
            
            addCity(cardID){
                this.cardCity.push({
                    citys:this.city,
                    cardID:cardID+1
                }),
                this.city=''
            },

            addImg(){
                this.img.src=this.cardImg[(this.counter)]
            },
          
            count(){
                //this.counter+=1
                
                for(let i=0; i<this.cardAll.length; i++){
                    this.counter++
                    
                }
                
            },

            lessThanID(k, idCount=0){
                idCount=this.counter
                console.log(idCount)
                for(let i=1;  i==idCount; i++){
                //let i=0
                //do{
                    return k.filter(function(j){
                        return j.cardID == idCount;
                    })
                }
                //}while(i<idCount)
            },
            /*whileCondition(){

            },*/

            redirect(){
                location.href = 'details';
            },
        },
    }
    
</script>

<style>

    .userCard{
        display: grid;
        width: 45%;
        display: inline-block;
        height:270px;
        right:15px;
        top: 0px;
    };

    .img1{
        width: 100px;
     };

</style>
