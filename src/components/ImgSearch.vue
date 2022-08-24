<template>
	<div id="">
        <p>
            <span class="text-primary">B</span>
            <span class="text-danger">o</span>
            <span class="text-warning">o</span>
            <span class="text-primary">l</span>
            <span class="text-success">l</span>
            <span class="text-danger">e</span>
        </p>
        <p class="subText text-light"><b>The fastest img search on the web! </b></p>
		<input type="text" @keyup.enter="search" v-model="searchTerm" placeholder="SearchField Sans Button" style="line-height:auto">
		<!--<button  @click="search" > OK </button>-->
	</div>
</template>
<script>
export default {
    name: 'ImgSearch',
    data(){
        return{
            searchTerm: '',
        }
    },
    methods:{
        search: function(){ 
            if(this.searchTerm.length > 0){
                let term = this.searchTerm.replace(/ /g,"+");
                let url = "https://www.google.com/search?as_st=y&tbm=isch&hl=nl&as_q="
                        + term + "&as_epq=&as_oq=&as_eq=&cr=&as_sitesearch=&safe=images&tbs=ic:trans,iar:s";
                window.open(url);
            }else{console.log("Dont vergeet ave zuktrem é");}
        }
    }
}
</script>
<style>
    p span{
        font-size: 60px;
        font-weight: 600;
        font-family: play;
    }

    .subText{
        color: rgba(0,0,0,0.5);
        font-size: 14px !important;
        font-style: italic;
        font-weight: 500;
        position: relative;
        top: -30px;
    }

</style>