<template>
  <PlantSearchVieuw/>
</template>

<script>
import PlantSearchVieuw from './views/PlantSearchVieuw.vue'

export default {
  name: 'App',
  components: {
    PlantSearchVieuw,
  }
}
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  padding-top: 60px;
  background-color: #343a40!important;
  width: 100%;
  height: 100%;
}

.btnn{
	position: absolute;
    width: 100px;
    height: 50px;
	text-align:center;
	vertical-align: middle;
	font-style: italic;
	background: #343a40!important;
	border: 3px ridge rgba(25,150,25,0.66);
	color: white;
	text-shadow: 1px 2px rgba(25,100,25,0.66);
	font-size: 15px;
	font-weight: bold;
}

.btnn:hover{
    transform: scale(1.5,1.5);
    box-shadow:  1px 1px black;
}

hr {
    margin-top: 1rem;
    margin-bottom: 1rem;
    border-top: 3px ridge rgba(25,150,25,0.66) !important;
    opacity: 1 !important;

}
</style>
