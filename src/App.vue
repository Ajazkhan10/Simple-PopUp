<template>
  <div>
    <main>
			<button @click="tttttt">click</button>
      <h1>PopUp</h1>
      <button @click="openPopUp">Open PopUp</button>
      <PopUp v-if="buttontriggle" :closePopUp="closePopUp" :buttontriggle="buttontriggle">
        <h3>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Eius ex illum
          sed saepe perferendis nulla soluta architecto deleniti, quae alias
          error at repellendus molestias dicta ipsam aliquam. Laboriosam, vel
          quaerat.
        </h3>
        <h2>My PopUp</h2>
      </PopUp>
			<PopUp1 v-if="timedTriggle" :closePopUp="closePopUp" :buttontriggle="buttontriggle">
        <h3>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Eius ex illum
          sed saepe perferendis nulla soluta architecto deleniti, quae alias
          error at repellendus molestias dicta ipsam aliquam. Laboriosam, vel
          quaerat.
        </h3>
        <h2>My PopUp</h2>
      </PopUp1>
    </main>
  </div>
</template>

<script>
import PopUp from "./components/PopUp.vue";
import PopUp1 from './components/PopUp1.vue'
export default {
  name: "App",
  components: { PopUp ,PopUp1},
  data() {
    return {
      buttontriggle: false,
      timedTriggle: false,
    };
  },
	methods:{
		openPopUp(){
			this.buttontriggle=true	
		},
		tttttt(){
			setTimeout(() =>{
        this.timedTriggle=true;
			},2000)
		},
		closePopUp(){
			this.buttontriggle=false;
			this.timedTriggle=false
		}
	}
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
