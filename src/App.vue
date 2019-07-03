<template>
  <v-app>
	  <Header></Header>		  
    <v-content>		
      <router-view/>	 
    </v-content>
	 <Footer></Footer>
	 <go-top :right="30" :size="60" bg-color="#c0c0c0"></go-top>	
  </v-app>
</template>




<script>
import store from './store'
import Header from './components/Header'
import Footer from './components/Footer'
import GoTop from '@inotom/vue-go-top'
export default {
	name: 'App',
	store,
	data() {
		return {
			//
		}
	},
	components : {
		Header,
		Footer,
		GoTop
	}
	
	
}
</script>
