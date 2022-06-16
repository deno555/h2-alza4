<template>
    <div v-for="(i) in card" :key="i.cardTitle">
      <ion-card @click="redirect()">
        <ion-card-header>
            <div class="images">
            <img class="img1" src="https://www.business2community.com/wp-content/uploads/2017/08/blank-profile-picture-973460_640.png">
            </div>
        </ion-card-header>

        <ion-card-content>
            <!--p>Meno</p>
            <p>Mesto</p>
            <p>Jaziky</p>
            <p>Plat</p>
            <p>Skusenosti</p-->

            <p v-for="j in lessThanID(cardAll)" v-bind:key="j.cardName" >{{j.names}} - {{j.cardID}}</p>
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
                cardName:[
                    {names:"Impostor", cardID:1},
                    {names:"Crewmate2", cardID:2},
                    {names:"Crewmate3", cardID:3},
                    {names:"Crewmate4", cardID:4},
                    {names:"Crewmate5", cardID:5},
                    {names:"Crewmate6", cardID:6},
                ],
                cardJob:[
                    {jobs:"Sus", cardID:1},
                    {jobs:"Electrical", cardID:2},
                    {jobs:"Water", cardID:3},
                    {jobs:"Vent", cardID:4},
                    {jobs:"Medical", cardID:5},
                    {jobs:"Admin", cardID:6},
                ],
                cardSkill:[
                    {skills:"Kill", cardID:1},
                    {skills:"Wires", cardID:2},
                    {skills:"Pipe", cardID:3},
                    {skills:"Air", cardID:4},
                    {skills:"Heal", cardID:5},
                    {skills:"Monitor", cardID:6},
                ],
                cardMoney:[
                    {moneys:21, cardID:1},
                    {moneys:22, cardID:2},
                    {moneys:23, cardID:3},
                    {moneys:24, cardID:4},
                    {moneys:25, cardID:5},
                    {moneys:26, cardID:6},
                ],
                cardCity:[
                    {citys:"Space1", cardID:1},
                    {citys:"Space2", cardID:2},
                    {citys:"Spcae3", cardID:3},
                    {citys:"Space4", cardID:4},
                    {citys:"Space5", cardID:5},
                    {citys:"Space6", cardID:6},
                ],
                cardImg:[
                    {imgs:"https://cdn.discordapp.com/attachments/768503373363806218/970768614942732388/unknown.png", cardID:1},
                    {imgs:"https://cdn.discordapp.com/attachments/768503373363806218/978195932485152778/unknown.png", cardID:2},
                    {imgs:"https://cdn.discordapp.com/attachments/768503373363806218/978195969126572052/unknown.png", cardID:3},
                    {imgs:"https://cdn.discordapp.com/attachments/768503373363806218/978196062022033439/unknown.png", cardID:4},
                    {imgs:"https://cdn.discordapp.com/attachments/768503373363806218/978196122126401546/unknown.png", cardID:5},
                    {imgs:"https://cdn.discordapp.com/attachments/768503373363806218/978196151826280499/unknown.png", cardID:6},
                ],
                cardAll:[
                    {names:"Impostor", jobs:"SUS",skills:"Kill", moneys:"21",citys:"Space1",cardID:"1"},
                    {names:"Crewmate2", jobs:"Electrical",skills:"Wires", moneys:"22",citys:"Space2",cardID:"2"},
                    {names:"Crewmate3", jobs:"Water",skills:"Pipe", moneys:"23",citys:"Space3",cardID:"3"},
                    {names:"Crewmate4", jobs:"Vent",skills:"Air", moneys:"24",citys:"Space4",cardID:"4"},
                    {names:"Crewmate5", jobs:"Medical",skills:"Heal", moneys:"25",citys:"Space5",cardID:"5"},
                    {names:"Crewmate6", jobs:"Admin",skills:"Monitor", moneys:"26",citys:"Space6",cardID:"6"},
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

    ion-card{
        display: grid;
        width: 38%;
        display: inline-block;
        height:270px;
        left:15px;
        top: 0px;
    };

    .img1{
        width: 100px;
     };

    .img2{
        position: absolute;
        width: 4px;
    };

</style>
