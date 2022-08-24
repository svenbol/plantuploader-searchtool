<template>
    <div class="container">
        <div class="row mt-2">
            <div class="col-12">
                <h2 class="text-light"><b>Easy Plant Info</b></h2>
                <p class="text-success"><b><i>
                    Hold CTRL to spamclick the buttons!
                </i></b></p>
            </div>
        </div>
        <div class="row mt-4">
            <div class="col-12 mx-auto h-60p"> 
                <input type="text" v-model="example" placeholder="Plantname Here" class="inputTxt d-block mx-auto">
            </div>
            <div class="col-12 mx-auto h-60p">
                <button class="btnn" @click="btnRemove(index);urlFamily(example)"> Family </button>
                <button class="btnn" @click="btnRemove(index);urlImg(example)"> Image </button>
                <button class="btnn" @click="btnRemove(index);urlHumidity(example)"> Humidity </button>
                <button class="btnn" @click="btnRemove(index);urlWatering(example)"> Watering </button>
                <button class="btnn" @click="btnRemove(index);urlPh(example)">- PH -</button>
                <button class="btnn" @click="btnRemove(index);urlSun(example)">- Sun -</button>
                <button class="btnn" @click="btnRemove(index);urlTempMin(example)"> Temp Min </button>
                <button class="btnn" @click="btnRemove(index);urlTempMax(example)"> Temp Max </button>
                <button class="btnn" @click="btnRemove(index);urlNutriWhat(example)"> Nutri What </button>
                <!--<button class="btnn" @click="btnRemove(index);urlNutriWhen(example)"> Nutri When </button>-->
                <button class="btnn" @click="btnRemove(index);urlNutriFreq(example)"> Nutri FreQ </button>
                <!--<button class="btnn" @click="btnRemove(index);urlPruningWhat(example)"> Prune What </button>-->
                <button class="btnn" @click="btnRemove(index);urlPruningWhen(example)"> Prune When </button>
                <button class="btnn" @click="btnRemove(index);urlRepotFreq(example)"> Repot FreQ </button>
                <!--<button class="btnn" @click="btnRemove(index);urlRepotWhen(example)"> Repot When </button>-->
                <!--<button class="btnn" @click="btnRemove(index);urlMaker(example)"> OTO MATIC </button>-->
            </div>
        </div>
    </div>
   
    
	
</template>
<script>
 export default {
    name: 'PlantSearch',
    data(){
        return{
            example: '',
            plantName: 'philo',
            urls:[
                {urlFamily: ""},
                {urlImg: ""},
                {urlHumidity: ""},
                {urlWatering: ""},
                {urlPh: ""},
                {urlSun: ""},
                {urlTempMin: ""},
                {urlTempMax: ""},
                {urlNutriWhat: ""},
                {urlNutriWhen: ""},
                {urlNutriFreq: ""},
                {urlPruningWhat: ""},
                {urlPruningWhen: ""},
                {urlRepotFreq: ""},
                {urlRepotWhen: ""}
            ]	
        }
	},
    props:{
    },
    methods:{
        urlMaker: function(){//function(plantName){
            //console.log("URL MAKER");
            //this.urlFamily(plantName);
            //console.log("2");
            //this.urlImg(plantName);

            var btnList = document.getElementsByClassName("btnn");
                console.log(btnList);
                console.log(btnList.length)

            for ( let i = 0; i < btnList.length; i++ ) {
                //setTimeout(document.getElementsByClassName("btn")[i].click(),2000);
                document.getElementsByClassName("btnn")[i].click();
			}	
        },
        urlFamily: function(plantName){
            this.urls[0] = "https://www.google.com/search?q=" + plantName + "+wiki";
            window.open(this.urls[0],'_blank');
        },
        urlImg: function(plantName){
            //if(plantName.length > 0){ alle code ertussen }
            let term = plantName.replace(/ /g,"+");
            this.urls[1] = "https://www.google.com/search?as_st=y&tbm=isch&hl=nl&as_q="
                        + term + "&as_epq=&as_oq=&as_eq=&cr=&as_sitesearch=&safe=images&tbs=ic:trans,iar:s";
            
            window.open(this.urls[1],'_blank');
        },
        urlHumidity: function(plantName){
            this.urls[2] = "https://www.google.com/search?q=" + plantName + "+humidity";
            window.open(this.urls[2],'_blank');
        },
        urlWatering: function(plantName){
            this.urls[3] = "https://www.google.com/search?q=" + plantName + "+watering";
            window.open(this.urls[3],'_blank');
        },
        urlPh:function(plantName){
            this.urls[4] = "https://www.google.com/search?q=" + plantName + "+ph+value";
            window.open(this.urls[4],'_blank');
        },
        urlSun:function(plantName){
            this.urls[5] = "https://www.google.com/search?q=" + plantName + "+sun+or+shade";
            window.open(this.urls[5],'_blank');
        },
        urlTempMin:function(plantName){
            this.urls[6] = "https://www.google.com/search?q=" + plantName + "+min+temp";
            window.open(this.urls[6],'_blank');
        },
        urlTempMax:function(plantName){
            this.urls[7] = "https://www.google.com/search?q=" + plantName + "+max+temp";
            window.open(this.urls[7],'_blank');
        },
        urlNutriWhat:function(plantName){
            this.urls[8] = "https://www.google.com/search?q=" + plantName + "+npk";
            window.open(this.urls[8],'_blank');
        },
        urlNutriWhen:function(plantName){
            this.urls[9] = "https://www.google.com/search?q=when+to+feed+" + plantName;
            window.open(this.urls[9],'_blank');
        },
        urlNutriFreq:function(plantName){
            this.urls[10] = "https://www.google.com/search?q=how+often+should+i+fertilize+my+" + plantName;
            window.open(this.urls[10],'_blank');
        },
        urlPruningWhat:function(plantName){
            this.urls[11] = "https://www.google.com/search?q=what+to+prune+" + plantName;
            window.open(this.urls[11],'_blank'); 
        },
        urlPruningWhen:function(plantName){
            this.urls[12] = "https://www.google.com/search?q=when+to+prune+" + plantName;
            window.open(this.urls[12],'_blank');
        },
        urlRepotFreq:function(plantName){
            this.urls[13] = "https://www.google.com/search?q=how+often+should+i+repot+" + plantName;
            window.open(this.urls[13],'_blank');
        },
        urlRepotWhen:function(plantName){
            this.urls[14] = "https://www.google.com/search?q=when+to+repot+" + plantName;
            window.open(this.urls[14],'_blank');
        },
        btnRemove: function(){//function(index){
            var btnList = document.getElementsByClassName("btnn");
                btnList[btnList.length-1].parentNode.removeChild(btnList[btnList.length-1]); 
        }
    }
}
</script>
<style scoped>
.row{
}

.inputTxt{
    height: 50px;
    line-height: 50px;
}

h2{
     font-family: sans-serif;
}

.h-60p{
 height: 60px;
}

p{
    margin: 0 !important;
}

input[type=text]{
    height: 50px;
    outline: none;
    background: transparent;
    font-size: 30px;
    margin: 0 auto;
    border: none;
    border-top-left-radius: 5px;
    border-top-right-radius: 5px;
    font-style: italic;
    color: white;
}
	
</style>