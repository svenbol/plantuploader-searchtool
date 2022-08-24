<template>
    <hr class="w-75 mx-auto">
	<PlantSearch></PlantSearch>

</template>
<script>
	import PlantSearch from "../components/PlantSearch.vue"

	export default {
        name: 'PlantSearchView',
        data(){
            return{
            }
        },
        components: {
            PlantSearch
        }
    }

</script>
<style scoped>
	/*template{
        background-color: #343a40!important
    }*/
</style>